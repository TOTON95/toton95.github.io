---
layout: post
title:  "TalentLand and Minidrones"
date:   2021-07-24 12:00:00 -0500
lang: en
lang-ref: talentland-and-minidrones
published: true
categories: code updates ros drones parrot
comments: true
---

![Me](/assets/img/posts/talentland_minidrones_2.jpg)

Hello again, I hope you are still well, with a good coffee by your side and settled in your favorite chair to work from home. 

In this post I am going to reveal the secret I left in the last topic, I am also going to talk about how I attended the different conferences during the course of the pandemic. All of them related to science and technology, some examples are the past All Things Open 2020, Nvidia's GTC 2021 and more recently TalentLand 2021.

## TalentLand 2021

This event has been held every year since 2018, and its purpose is to bring together students, technology lovers and industry professionals in one place. Because of the pandemic, it was not possible to hold the event in person as was done in past editions, however in this conference, as in others that have been held in this period of contingency, were held virtually and often even for free and with other infrequent opportunities for attendees, so I recommend being attentive to the emergence of these chances, because although the experience is not the same, it allows access to quality material that is not possible to concentrate in other conditions that are not in conferences.

For TalentLand 2021, specifically, I thank Ramon Roche ([@mrpollo](https://twitter.com/mrpollo?s=20)) for the opportunity, Roche is Product Manager of the Foundation Dronecode, this foundation is who manages and maintains the [PX4](https://px4.io/) platform. At TalentLand 2021, Roche gave a very good introspection and history of the foundation and how Open Hardware and Source have permeated the industry. As a side note, I have also worked with PX4 in my experiments before and which I hope to share something from them along with their interaction with ROS and ROS2 in the future.

The event itself seems to me a great idea for young people in Mexico and LATAM, for this edition they were able to bring high level people for their respective fields, among them were Steve Wozniak, Adam Savage, Seth Godin and John Cohn. On the other hand, also participated characters of the maker community such as Ana Karen Ramirez ([@anaqueenmaker](https://www.instagram.com/anaqueenmaker/)) and Ricardo Muñoz ([@nquehmx](https://www.instagram.com/nquehmx/)).

All the activity was divided into different tracks, which were depending on the target audience of the topics to be discussed, being Business Channel for those interested in finance, investments and business styles such as E-Commerce; Developer Channel for those who are dedicated to Artificial Intelligence, DevOps and Cybersecurity; Creative Channel for artists and content generators; Blockchain Channel aimed at CryptoMonedas and NFTs; Iron Channel sought to focus on makers, IoT and robotics; Gamer Channel that covered everything related to the creation, distribution and consumption of video games; Superpoderes Channel was focused on the creation of good habits and interpersonal and intrapersonal skills; finally we have Talent World Channel that was for specialized topics. In addition, there were also two workshops Workshop Tech and Human, which taught topics in an interactive way related to the hard skills of technology and the soft skills of human relations, respectively.

The event itself was very entertaining and allowed me to understand the current state of the technology sector in Mexico and Latin America, I could see how important names in the industry considered the location of this region as important for the development and manufacture of technology products.  

Although at the beginning of the event what was apparently the organizers' plan A ended up not being possible (as a considerable amount of complaints were reported on social media), they were quick to establish a backup plan for the event. So kudos there for the team's planning and reaction.

Another aspect I liked was the ability to do networking among event attendees, this activity was done through the official app. The way it was handled, however, was something out of the ordinary, I do not know if it is the right way to manage possible interactions between people, and I say this because their solution was a similar style to Tinder (I have been told) and it could get difficult to choose the right words to make yourself known in such a short space and this if they were to read it, as it was very easy to be sliding from left to right at high speed. However, I found the talks with the community very good and it helped me to understand a little more about the internal inertia of the industry and academia.

Overall, I thought the speakers were pretty good in the way they communicated their topics, as well as motivating people who were interested in each of the fields, I spent most of the time on Developer and Iron Channel (I don't think anyone imagined that). A bonus was that each of the sessions was recorded for On-Demand use, which is nice and will keep me entertained for quite some time (unless I watch it all at once, haha). 

To close, I plan to come back next year, I hope and this time it will be in person even if it's just to live "the full experience", something that is highly recommended by other attendees. In the meantime, I share with you other conferences that I plan to attend during the rest of the year, these are SIGGRAPH 2021 (courtesy of Nvidia), PX4 Developer Summit 2021 and All Things Open 2021.

So let me know if you are going to attend these events, so we can exchange ideas and observations, you can also share if I am missing any conference that you consider important.

## Vision for ros_pyparrot

In this time I've been dedicating myself to the improvement of my repositories, specially in the code for the Parrot Mambo Minidrones, I hope you were able to find the answer to the secret of the previous post, and if the title and image haven't told you yet, I tell you that you are most probably right, I have managed to make the Minidrones serve you an espresso macchiato in record time ☕🤓 (well not for now but in the future I hope so). 

Being serious, actually it was the addition of the code for the onboard camera that is on the drone (you can see it in the following image), and on second thought, it is necessary to serve you that delicious coffee, for now I will focus on making it work correctly, debug any bugs and try to use some techniques to make the flow of images as close to real time as possible. This is very important, because without it the drone will not be able to obtain important information from its environment, such as its position in space, the existence of obstacles, targets to reach, among others. All this would be obtained out of phase to what it actually has, and that can translate directly into a very poor performance, more effort for position estimation and control strategies, but above all, a significant number of crashes and accidents that both you and your budget will resent (and maybe you would like to be cutting onions ... to disguise it).  

![ROS Pyparrot Artwork](https://toton95.github.io/assets/img/posts/ros-pyparrot_7.jpg)

So at the end of the story, these efforts are very important to keep those tears out of the scheme and better left for your own experiments using this interface. While it is not quite complete yet, it is already at an operational stage to start experimenting in a controlled environment. When I say that it is incomplete, I'm talking about a detail that I have to document more for its correct solution, the problem lies in the way the drone allows the transmission of data from the camera to the client that requests it, as it seems to have an internal timer that pauses the image stream, this is only restored when requesting the drone to move with the commands to operate the motors, and once stopped the timer eventually ends and the images stop. Apparently, it is not far from Parrot's initial idea, since in the official application the same thing seems to happen, this makes me suspect that it is a way to save energy, which seems to me sensible and more for the size of the Minidrone and its battery.

However, I would like to know if it is possible to keep the transmission open uninterrupted for practical purposes, as it was possible with Parrot Bebop and Bebop 2. For the time being, I will put a mechanism to recognize that no new frames have been received and send a signal to the ROS environment. On the other hand, for the user I will add an image that indicates the drone has not received new images and possibly some coding at the beginning of the image so that the programs that depend on only the image (I might remove it at the end, I will see how it behaves). Also, I will thoroughly investigate the ports exposed by `nmap` and see if there is a possibility to get this feature.

Another limitation to consider at the moment is that the camera only acts as an `Access Point` or `AP` and therefore the impossibility to keep the stream open and change the mode of the WiFi adapter could only be eliminated by modifying the firmware, which is not always convenient.

Once I had the new operating node for the drone vision, I decided to take a look at the [Twitter](https://twitter.com/alexis_guijarro/status/1415558596633391104?s=20) community, who have accepted very well the way I am developing the tool. At the time of writing this article, the tweet already has more than 4000 interactions and allowed me to talk to the author of the code base (`pyparrot`, by Dr. Amy McGovern) that I used to create my `ros-pyparrot` project. This helped me to understand a little better how she reasoned to create her code and what experiences she gained during the development, hence opening me to other options that I may explore in case they are needed or the workload is not too heavy.

This tweet also allowed me to be part of ROS weekly news again, which I feel is good, as it recognizes and spreads the efforts of the people who develop around the platform.  

Finally, I hope to bring new news about the GoPro driver for ROS, as well as a new sample experiment for `Mambo_ROS_Examples` that makes use of the new vision node on the Parrot Mambo drone.

In the meantime, let's keep waiting for that espresso macchiato. 🤤

