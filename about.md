---
layout: page
title: About
permalink: /about/
---

<!---This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](https://jekyllrb.com/)--->

Navigation: <a href="#Summary">Summary</a> \| <a href="#Research">Research</a> \| <a href="#Publications">Publications</a> \| <a href="#Portfolio">Portfolio</a> \|  <a href="#Projects">Projects</a> \| <a href="#Workshops">Workshops</a> <br><br>

<div style="text-align: right"> Downloads: <a href="/assets/pdf/cv_alexis.pdf" target="_blank" rel="noopener noreferrer">Resumé (PDF)</a></div>

## <a id="Summary">Summary</a>

<div style="text-align: justify">Gabriel Alexis Guijarro Reyes was born in Torreon, Coahuila, Mexico in 1995. He obtained his B.S. in Mechatronics and Process Control Systems Engineering in 2018 at Universidad La Salle Laguna, Gomez Palacio, Durango, Mexico. Later, he obtained a M.S. in Computer Science in 2020 at Texas A&M University Corpus Christi under Dr. Luis Rodolfo Garcia Carrillo and Dr. Scott A. King supervision. Currently, he is studying a PhD in EE at New Mexico State University, under Dr. Garcia Carrillo's supervision.</div><br>

## <a id="Research">Research</a>

My research fields are:

- Control Systems 

- Multi-Agent Systems

- Unmanned Aircraft Systems

- Robotics

- Computer Vision

- Linux Development

- ROS Development

  

## <a id="Publications">Publications</a>

1. Ignacio Rubio Scola, **Gabriel Alexis Guijarro Reyes**, Luis Rodolfo Garcia Carrillo, João Pedro Hespanha, Laurent Burlion, "A Robust Control Strategy With Perturbation Estimation for the Parrot Mambo Platform", IEEE Transactions on Control Systems Technology, September 2020. [[DOI]](https://doi.org/10.1109/TCST.2020.3020783)
2. I. Rubio Scola, **G.A. Guijarro Reyes**, L. R. Garcia Carrillo, J. Hespanha and J. Xie, “Translational Model Identification and Robust Control for the Parrot Mambo UAS Multicopter”, IEEE Globecom Workshop on Computing Centric Drone Networks, Hawaii, USA, December 2019. [[DOI]](https://doi.org/10.1109/GCWkshps45667.2019.9024528)
3. **G.A. Guijarro Reyes**, L.R. Garcia Carrillo, I. Rubio Scola, J. Martinez, J. Baca, and S.King, “Human gesture-triggered control actions for Unmanned Aircraft Systems: A Deep Neural Network-Inspired Approach”, Latin American Congress on Automation and Robotics (LACAR), Cali, Colombia, November 2019. [[DOI]](https://www.google.com/url?q=https%3A%2F%2Fdoi.org%2F10.1007%2F978-3-030-40309-6_10&sa=D&sntz=1&usg=AFQjCNHACyCL28VYDaQwyskc2SC4UhqmBQ)
4. B. Wang, J. Xie, Y. Wan, **G.A. Guijarro Reyes**, and L.R. Garcia Carrillo, “3-D Trajectory Modeling for Unmanned Aerial Vehicles”,  AIAA Science and Technology Forum and Exposition, January 2019, San Diego CA, USA. [[DOI]](https://www.google.com/url?q=https%3A%2F%2Fdoi.org%2F10.2514%2F6.2019-1061&sa=D&sntz=1&usg=AFQjCNHHDARh2hhAklzNB8wNNMIBxNqkyQ)
5. **G.A. Guijarro Reyes**, L.R. Garcia Carrillo, and P. Rangel. “A Geometric Control Strategy for Real-Time Coordination of Multiple Unmanned Aircraft Systems”,  2018 International Conference on Unmanned Aircraft Systems, June 2018, Dallas, TX, USA. [[DOI]](https://www.google.com/url?q=https%3A%2F%2Fdoi.org%2F10.1109%2FICUAS.2018.8453484&sa=D&sntz=1&usg=AFQjCNF3AghhIKSpWosXaqAAybwjLzIcDw)

<div style="text-align: center"><a href="https://scholar.google.com/citations?user=I32SQJkAAAAJ&hl=en&oi=ao" target="_blank" rel="noopener noreferrer"><h3>
    Visit my Google Scholar Profile
    </h3></a></div>


## <a id="Portfolio">Portfolio</a>

<div style="text-align:center">  
    <iframe width="100%" height="403" src="https://www.youtube.com/embed/ZNKXFGFx2Xo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

<div style="text-align:center">  
    <iframe width="100%" height="403" src="https://www.youtube.com/embed/cCiboUIuOSs" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

<div style="text-align:center">  
    <iframe width="100%" height="403" src="https://www.youtube.com/embed/3VxMfX5imto" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

<div style="text-align:center">  
    <iframe width="100%" height="403" src="https://www.youtube.com/embed/VW3uOdUgaac" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

#### **Title**: 

A Robust Control Strategy With Perturbation Estimation for the Parrot Mambo Platform

#### **Authors**:

Ignacio Rubio Scola, **Gabriel Alexis Guijarro Reyes**, Luis Rodolfo Garcia Carrillo, João Pedro Hespanha, Laurent Burlion

#### **Abstract**:

<div style="text-align: justify">This article addresses theoretical and practical challenges associated  with a commercially available and ready-to-fly small-scale unmanned  aircraft system (UAS) developed by Parrot SA: the Mambo quad rotorcraft. The dynamic model and the structure of the controller running onboard  the UAS autopilot are not disclosed by its manufacturers. For this  reason, a novel robust controller for discrete-time systems under time  delays and input saturation is first developed for this platform. Then,  three fundamental estimation and control challenges are addressed. The  first challenge is the system identification of the X and Y  translational dynamics of the UAS. To accomplish this goal, input-output data pairs are collected from different UAS platforms during real-time  experimental flights. A group of dynamic models are identified from the  data pairs through an extended least-squares algorithm. The obtained  models are similar in nature but exhibit parametrical variations due to  uncertainties in the fabrication process and different levels of wear  and tear. Using a time-varying modeling approach, the second challenge  addresses the development of a robust controller, which guarantees the  stability of all the identified dynamic models. The third challenge  addresses the development of a nonlinear controller enhanced with a  perturbation estimation, which can reject, from the nominal model, the  effects of model uncertainties and perturbations. These theoretical  developments are presented in the form of two original theorems. The  proposed strategies are ultimately validated in a set of real-time  experiments, demonstrating their effectiveness and applicability.</div>

<br>





<div style="text-align:center">  
<iframe width="100%" height="403" src="https://www.youtube.com/embed/3ryXO9mXObI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>



#### **Title**: 

Deep Neural Network-Inspired Approach for Human Gesture-Triggered Action Control applied to Unmanned Aircraft Systems 
#### **Authors**: 

**Gabriel Alexis Guijarro Reyes**, Juan Martinez, Luis Rodolfo Garcia Carrillo, Ignacio Rubio-Scola, Scott A. King, and Jose Baca. 

#### **Abstract**: 

<div style="text-align: justify">Deep Neural Networks have positively impacted the development of autonomous navigation strategies, allowing the integration of object detection capabilities to the vast array of already existing control methods. In this project, a Deep Neural Network is implemented to distinguish particular hand gestures, as well as user's arm movement, in order to trigger a specific activity of an Unmanned Aircraft System. We present real-time experimental results of how this technique is applied, making use of a Natural User Interface to control a the autonomous aircraft. </div>

<br>



<div style="text-align:center">  
<iframe width="100%" height="403" src="https://www.youtube.com/embed/lYeh9g84asI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<div style="text-align:center">
    <iframe width="100%" height="403" src="https://www.youtube.com/embed/HPLOlbfEVJA" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>




#### **Title**: 

A Geometric Control Strategy for Real-time Coordination of Multiple Unmanned Aircraft Systems

#### **Authors**: 

**Gabriel Alexis Guijarro Reyes**, Luis Rodolfo Garcia Carrillo and Pablo Rangel. 

#### **Abstract**:

<div style="text-align: justify">In recent years, the application of Unmanned Aircraft Systems (UAS) has incremented due to their cost-effectiveness ratio, portability and reduced size. This allows their utilization in multiple operations in complex military and civilian applications. UAS operations sometimes require the usage of human pilots to manage the different situations that can be present at any moment of a mission, and to decide the better option for every UAS involved. The simplest way to realize these tasks is to gather multiple pilots, one for each UAS. However, this option carries the complexity of coordinating the actions of every pilot involved in the mission. This might require several hours of specialized training, delays, and higher costs. To mitigate these nuances, this paper proposes a geometric control method to stabilize multiple UAS in formation. Our method allows a group of UAS to accomplish tasks using a determined formation. Two experiments are presented that demonstrates the performance of the technique. In the first experiment, one UAS is configured as a leader, while a second UAS is configured as a follower. The second experiment considers a scenario where the leader UAS is replaced by a physical device that can be used by a non-trained human pilot to directly affect the behavior of the follower UAS.</div><br>

## <a id="Projects">Projects</a> 

- [Bebop ROS Examples](https://github.com/TOTON95/Bebop_ROS_Examples) 
- [Hand Gesture UAV](https://github.com/TOTON95/Hand_Gesture_UAV)
- [Arduino Drawing Robot OpenCV-OpenNI](https://github.com/TOTON95/Arduino_Drawing_Robot_OpenCV_OpenNI)
- [ROS pyparrot](https://github.com/TOTON95/ros_pyparrot)

## <a id="Workshops">Workshops</a>

- [ROS Workshop Python CPP](https://github.com/TOTON95/ROS_Workshop_Py_CPP)
- [ROS Image Workshop](https://github.com/TOTON95/ros_image_workshop)
- [ROS Vicon Workshop](https://github.com/TOTON95/ros_vicon_workshop)



<!--You can find the source code for Minima at GitHub:-->
<!--[jekyll][jekyll-organization] /-->
<!--[minima](https://github.com/jekyll/minima)-->

<!--You can find the source code for Jekyll at GitHub:-->
<!--[jekyll][jekyll-organization] /-->
<!--[jekyll](https://github.com/jekyll/jekyll)-->


[jekyll-organization]: https://github.com/jekyll
