---
layout: post
title:  "Art, code and updates"
date:   2021-07-09 01:00:00 -0500
lang: en
lang-ref: art-code-and-updates
published: true
categories: art code updates ros
---



![Artwork banner](/assets/img/posts/art-code-and-updates.png)

Since the last post I have dedicated myself to updating and maintaining my codes on GitHub. This due to my purpose of bringing my knowledge to more people, I have made several actions to make it more attractive. Part of this has fallen into adding art for dissemination through social networks, with which I hope I can increase the exposure of these contributions to the community.


## The art

The art that I have so far is distributed throughout this post, I hope that its function has been fulfilled and you have dedicated yourself to observe them first before starting with the text.

For the realization of these drawings I used the Clip Art Studio program, which is used for the creation of drawings, comics and manga, so it turns out to be the best candidate for the job, that and I had not been able to find the perfect excuse to use it since I bought it. 

Also, I have proven once again how therapeutic making art is, as well as taking pictures, they have my seal of approval 🤓. 

Now, speaking of the inspiration for this style of art, I based it on the labels I've seen on people's laptops, and although I don't use them on mine (I like to keep the original exterior of my computers) but I like to see the level of personalization and visual appeal they cause in those who look at them, so I wanted to copy that effect in my art. 

The addition of new art is going to be added intermittently, as I need to pick up some pace to finish backlogged projects, but eventually I will cover all the major repositories. 

As always, I am infinitely grateful for your feedback on the images.

## The code

Each of the illustrations gives image to the most visited repositories by the community since I started my journey through the ROS or Robot Operating System platform. For those who don't know it, this tool works as Middleware, in other words, it is the translator between Software and Hardware, and in practical terms it helps us to have an easy and better communication between the nodes (programs that control each of the functions in ROS) in a distributed way. Each of these nodes helps you to separate the components of a robot and its software controller by their tasks, source or destination. Each of these nodes can be focused on either data acquisition through sensors, actuator action, information processing, or a node controller that is responsible for managing the interaction between two or more nodes. I like to see it as a kind of "glue", as it helps you to split a giant problem into smaller and easier to handle problems. 

![Bebop_ROS_Examples_image](https://toton95.github.io/assets/img/posts/BebopROSExamples_3.jpg)

### "Bebop_ROS_Examples"

The first illustration is about my first repository made with a collection of experiments that I made together with my classmates during my stay at Texas A&M University in 2017. I have a special fondness for this code, as it was the one that led me to have my first followers and start appearing in the sights of several developers and teachers about the field. The collection is designed for the Parrot Bebop drone (and in theory is compatible with Parrot Bebop 2) and contains code for open-loop experiments, multi-vehicle experiments, and other exercises using a motion capture system.

Finally, for 2018, the collection received its last addition to document code for the National Robotics Tournament competition in Mexico, specifically in the autonomous aerial vehicle category, where second place was achieved for the object tracking exercise, and our solution was the best in the competition. 

![ROS Pyparrot Artwork](https://toton95.github.io/assets/img/posts/ros-pyparrot_7.jpg)

### "ros_pyparrot"

This repository was created to form a platform of drones small enough to operate as a group and execute commands independently. Other factors such as the size of the flying area and cost influenced the choice of the Mambo Parrot as the main target. 

The code as a whole, works just like a "driver", meaning that it coordinates communications between the computer and the drone in order to perform the requested actions. When I did some research about it, I found that the traditional method of communication with cell phones or tablets was via Bluetooth and WiFi, with which I felt very comfortable, as I had worked with it on another occasion. However, upon further investigation, I discovered that I was using the most recent Bluetooth version, which at that time was 4.0, which introduced a form of energy-saving transmission, formally called Bluetooth Low Energy (BLE). 

The major difference between the version I used and BLE is that you need to "wake up" and "keep awake" the communication path between both ends of the transmission. This presented me with a new challenge, so I set about researching some means of communicating the Mambo Parrot with ROS or some SDK that I could make use of for my experiments. 

Unfortunately, my efforts to find something already done failed, so the only hope I had left was to try to do Reverse Engineering, so I invested in a BLE Sniffer, a tool to intercept the packets sent between both ends of the transmission and a personal Mambo Parrot in case I broke it (the drones I was going to work on were from the university).

The first efforts yielded few results, but they helped me to better understand the behavior of the drone, as well as to know how this version of Bluetooth worked, without having to study much of the official manual. Soon after, and within the conversations in several forums about the Reverse Engineering on this drone, I came across the work of Dr. Amy McGovern, who already almost figured out everything needed to make the drone work, the name of her [project](https://github.com/amymcgovern/pyparrot) is `pyparrot`. 

A quick look and test later convinced me to create an interface between her work and the ROS platform, based on what Autonomy Lab had established with `bebop_autonomy`. Soon after, I got the results I was looking for, and was even able to include functionality that had not yet been added, such as auto takeoff, where you launch the drone into the air to keep it flying. Thanks to ROS, it was possible to launch up to 8 drones at the same time (per BLE specs). Seeing all those drones flying, I called it a success and went to sleep.

I'm still waiting to add a couple of features I'm missing....

![Mambo ROS Examples Artwork](https://toton95.github.io/assets/img/posts/Mambo_ROS_Examples_2.jpg)

### "Mambo_ROS_Examples"

This repository is the spiritual successor of "Bebop_ROS_Examples", which contains several of those experiments but improved and others involving two or more drones. The project was based entirely on the needs of testing the drone itself and performing the experiments for a conference paper in ["IEEE Globecom Workshop on Computing Centric Drone Networks" ](https://doi.org/10.1109/GCWkshps45667.2019.9024528) and an entry to the Journal ["IEEE Transactions on Control Systems Technology"](https://doi.org/10.1109/TCST.2020.3020783). 

I needed quite some time to complete this series of experiments, however, I am glad I did it and also took the time to do it right, as both this repository and the previous two are serving as support material for students at various universities around the world, and I can tell by who follows them and the season in which they are viewed or cloned.

I hope to be able to continue expanding this project soon. 

![ros-gopro-driver Artwork](https://toton95.github.io/assets/img/posts/ros_gopro_driver_6.jpg)



### "ros-gopro-driver"

Finally, this is the newest ROS repository I have published, almost like with `pyparrot`, I did not find a way to record my experiments with my GoPro and ROS independently (they were part of other packages and only certain functions), without having to get inside the test area to start recording. Sure, I could use the smartphone app, but sometimes I used it to monitor other things in the experiment, location data, status, among other things. 

So I had to get used to it until I finished my master's degree. After I moved to Las Cruces, New Mexico, I had the time to work on it again, soon after I found a [WiFi API collected by KonradIT]( https://github.com/KonradIT/goprowifihack), it was there that I found a direct way to interact with the cameras through the Python `requests` library and extend the commands and information to ROS. 

Up to this point, I was already able to manage the camera and make use of several of the camera's main functions, now I just needed to find a way to stream live video to include it within ROS. Fortunately, I had already had some time playing with the [FFMPEG](http://ffmpeg.org/) project and [Leandro Moreira](https://github.com/leandromoreira/ffmpeg-libav-tutorial) tutorials (which I helped to translate into Spanish, as appreciation), and it was these tools that put me on the right track to capture and decode each of the packets that are received at the highest possible speed, comparing similarly to what is delivered in the official application, at least subjectively (more tests will be done in the future).

The code was ready and I just needed to test it, to my luck it worked great, of course there were several regions with pixel corruptions but they were the same in the official application, so my theory focuses on the quality of the WiFi antenna connection (I'm considering consulting Leandro for any idea).

I just needed someone to test it on their computer to confirm that the same result could be reproduced, so I decided to send it to my friend [Evan Krell](https://github.com/ekrell) from Texas A&M University - Corpus Christi, who confirmed it worked, made practical use of the program in his [project](https://ekrell.github.io/underwater-gopro-stream/) and became a contributor to the repository, with all that evidence I made a Tweet with the current status of the code... and the community loved it. 🖤

They loved it so much that we were featured in the [ROS weekly roundup](https://discourse.ros.org/t/ros-news-for-the-week-of-2-19-2021/19051) and some time later in an [Ubuntu article](https://ubuntu.com/blog/the-state-of-robotics-february-2021). It was amazing, and to top it off we were published in the same week that Perseverance and Ingenuity had landed on Mars, so we were second in clicks (first after the Mars news).

This motivated me to try to push the limit a bit more to accept more cameras and functionalities in the future, as well as to see how to contribute to the ROS 2 source code, since it has been made public its use in the 2023 lunar mission by NASA, and I want to be able to contribute to something like that (that and for the success of Perseverance and Ingenuity on Mars, they were giving away special badges to all contributors of the Open Source libraries used in the mission).

## ... and updates

Now in terms of code updates, I have been working on maintaining old code as well as adding new features for the GoPro camera driver with ROS such as getting the camera status, making a log that relates videos to experiments automatically, all in order to finish the pending projects and jump to the next version of the platform, ROS 2.

At this point, I will take some time to understand more about the internal mechanism of ROS 2, which I hope to increase my knowledge about the platform and make the necessary decisions for the migration of my most important repositories. However, it is important to know that it is possible to intertwine nodes from both versions, so there is always the possibility of continuing with just keeping the tools in ROS and not carrying out the migration.

## Before you go, a final message:

If you have a keen eye and have reviewed the repositories and images presented here, you will notice a surprise update that is about to be released to the public. 

Also within this secret (temporary) environment, I tell you that I have several backlogged projects in which I will resume my development efforts, they are going to take a while, and more with the new knowledge additions thanks Nvidia and their GTC 2021 event. 

Also at the moment I'm finishing writing this post, I just attended to TalentLand 2021, an event where important tech companies and people go to instruct and coach students to get into this world, I will talk more about it at the next post.

I hope you enjoyed reading this, now let's enjoy a good coffee.... ☕
