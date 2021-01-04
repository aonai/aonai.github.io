---
title: Fast Tower
intro: Using a Baxter robot to build a tower of cups.
layout: default
# modal-id: 1
date: 2020-11-01
time: November, 2020
video: https://www.youtube.com/embed/HEcnxoLQmnU
img: 10-cups-whole.gif
urls:
    - 
        url: https://drive.google.com/drive/folders/1TNZ8SyosjOLlZyvqhP1VXR4JyEkqHliD?usp=sharing
        url-description: Other Video Demos
        url-icon: fa-folder
    - 
        url: https://github.com/aonai/final-project-fast-tower.git
        url-description: Source Code
        url-icon: fa-github
members: Dimitrios Chamzas, Dongho Kang, Gabbie Wink
skills: Baxter, ROS, MoveIt!, Apriltag
description: This poject is the final project of Embedded Systems in Robotics. Its goal is to control a Baxter robot to stack a fixed number of cups into a tower. The tower is built on a table that is placed in front of Baxter. The source code includes several different nodes to operate Baxter with or without computer vision and to build a tower out of 3, 6, and 10 cups. More detailed descriptions can be found on project's GitHub page. To minimize challenge from vision detection and precise manipulation, this porject is separated into two tasks. Starting with random cups placed in the middle of table, task 1 needs to grab and place them at each side of table in order. Then, task2 needs to grab the sorted cups and place them back to middle of table to stack them into a tower. The image below shows how a table is divided into working area and sorted area. <img src="img/portfolio/fast-tower-table.png"> For this project, my main job is to control both arms of Baxter to let them grab and place cups from one to another specified location. The locations are either pre-defined or provided by Apriltags depending on whether the node uses computer vision. The image on the left below shows Baxter grabbing a sorted cup. The image on the right below shows Baxter placing the cup into work station. The movement of Baxter arm is controlled using ROS <a target="_blank" rel="noopener noreferrer" href="http://docs.ros.org/en/hydro/api/baxter_interface/html/baxter_interface.gripper.Gripper-class.html#version_check">MoveIt</a> package for Baxter. The gripper is controlled using <a target="_blank" rel="noopener noreferrer" href="http://docs.ros.org/en/hydro/api/baxter_interface/html/baxter_interface.gripper.Gripper-class.html#version_check">Baxter ROS interface</a>. <img src="img/portfolio/fast-tower-single-grab.gif" style="width:40%" float="left">  <img src="img/portfolio/fast-tower-single-place.gif" style="width:41%" float="left"> To limit unexpected behavior of Baxter while using path planning with pose target, the team uses cartesian planning methods provided by MoveIt to control behavior of the arms and add a short settlement time in between each move. Also, to avoid collision between the two arms, they are controlled alternatively. Once one arm completes placing a cup, it should move away from middle of table and leave work space for the other arm. 
---
