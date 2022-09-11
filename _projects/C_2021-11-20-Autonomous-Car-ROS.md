---
title: Autonomous Car ROS
layout: post
date: 2021-11-20 00:01
tag: 
- ROS
- C++
- OpenCV
- PCL

description: "A Prius drives through a delimited path and stops at the sight of humans"
category: project
author: yohanlegars
externalLink: false
---

<img src="../../assets/uploads/prius_project.png" width="1300" height="300"/> 

<div  style = "text-align: justify">
<p>
University assignment that consisted of developping software for autonomous driving of a prius vehicle in a simulated test track using ROS. The prius has two main sensors: a front-facing camera behind the windscreen and a 360 degree top mounted lidar. The vehicle receives camera images and lidar pointclouds as ROS topics.  
</p>
<p>
A virtual controllable Prius vehicle must use its sensors to detect obstacles and pedestrians, and use these detections to drive automatically between a path outlined by cones, without hitting any obstacle. The vehicle must stop at the sight of pedestrians.
</p>
<p>
The simulator (car and environment) being provided by the university, three additional ROS packages have been implemented as a solution.</p>
<ul>
<li>An <strong>opencv_person_detector</strong> package, containing the node to detect 2D bounding boxes of all persons in a camera image using OpenCV.</li>
<li> A <strong>pcl_obstacle_detector</strong> package, containing the node to detect 3D bounding boxes of all barrels in the lidar pointcloud using PCL.</li>
<li> A <strong>control_barrel_world</strong> package, containing the node to control the vehicle, by subscribing to 3D barrel detections and 2D person detections and publishing control messages.</li>
</ul>
<p>
The following figure displays the topics and nodes present in the solution.
</p>
<img src="../../assets/uploads/prius_solution.png" width="581" height="328"/> 

<p>
The source code for this assignment must remain undisclosed. 
Below is a blurry recording of the working simulation after the solution has been implemented. The gif makes the display lag a bit.
</p>

</div>


<img src="../../assets/uploads/prius_project.gif" width="1300" height="300"/> 





