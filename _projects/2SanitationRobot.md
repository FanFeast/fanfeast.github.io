---
title: "Sanitation Robot"
collection: projects
permalink: /projects/p2
excerpt: 'Independent Group Project [June 2020 - February 2021]'
---
[[report]](https://drive.google.com/file/d/1jr6RCCDWNcdROn00SAsmR9s1Q2w9nzuz/view?usp=share_link)
* <b>Tech Stack:</b> Python, V-Rep(coppeliaSim), SolidWorks
* <b> Summary </b>
    -  Created a CAD design and prototype of a sanitation robot as a team lead of twelve students
    -  Analyzed stability and implemented trot, canter and pace gait to analyses the various performance
    -  Redesigned the legs of the quadruped robot making it capable of performing backflips; conducted kinematic workspace analysis of the robot and using the kinematic equation of motions and Simulink

* <b>In-Depth</b>
    * <p style="text-align: justify;"><b>Introduction</b><br>The purpose of this project is to develop a modular sanitation robot that can be easily upgraded or downgraded by adding or removing specific blocks. The aim is to provide a cost-effective solution to customers, as they won't have to buy an entirely new robot to make changes in its features. This was accomplished by creating a robot that will include specialized blocks designed for specific purposes like motor and sensor controllers, wiring for camera and input, dry/wet mop, vacuum, and UV light sanitation.</p>
    
    <div style="text-align:center">
    <img src="/images/Sanitation_Robot_1.png" alt="Robot_Render" style="width:700px;height:300px;">
    </div>
    <figcaption style="text-align: center;"><u><em>Fig-1 Pioneer3DX robot</em></u></figcaption>
    
    * <p style="text-align: justify;"><b>Mechanical Design</b><br>We used the older robot design called Pioneer3dx (Fig-1) as the base for our sanitation robot and then made significant upgrades to its design. We divided the robot into modular blocks (as seen in Fig-2), and each block was designed to perform a particular task. Block 1 contained the robot's motor and sensor controllers and battery, block 2 included sensors and wiring for camera and input, block 3 was responsible for dry, wet mop and vacuum, and block 0 was the UV light sanitation module.</p>
    
    <div style="text-align:center">
    <img src="/images/Sanitation_Robot_2.png" alt="Robot_Render" style="width:500px;height:450px;">
    </div>
    <figcaption style="text-align: center;"><u><em>Fig-2 Render of the Sanitation Robot</em></u></figcaption>
    
    * <p style="text-align: justify;"><b>Working</b><br>The sanitation robot had two modes of operation, i.e., systematic clean-up (as shown in Fig-3) and random (as can be seen in simulation-1). The systematics clean-up mode was triggered when the room was empty, and the robot followed a fixed path while sanitizing and mopping the entire place using the A*Star algorithm. On the other hand, the random mode enabled the robot to move randomly without colliding with objects/obstacles and humans.</p>
    
    <div style="text-align:center">
    <img src="/images/Sanitation_Robot_3.png" alt="Robot_Render" style="width:500px;height:450px;">
    </div>
    <figcaption style="text-align: center;"><u><em>Fig-3 Systematic clean-up path for the robot</em></u></figcaption>
    
    * <p style="text-align: justify;"><b>Conclusion</b><br>In conclusion, we successfully designed and built a modular sanitation robot that could be easily upgraded or downgraded by adding or removing specific blocks. We sold nine prototypes of the robot to initial investors, particularly those who owned libraries and gyms, as they would benefit the most from such a product. The robot's two modes of operation, i.e., systematics clean-up and random, provided flexibility in its functionality, making it a reliable and effective solution for customers.</p>
    
    <div style="text-align:center">
    <video src="/images/Sanitation_Robot_Video.mp4" controls="controls" style="width:750px;height:500px;"></video>
    </div>
    <figcaption style="text-align: center;"><u><em>Simulation-1 Random Motion capabilities of the Robot</em></u></figcaption>