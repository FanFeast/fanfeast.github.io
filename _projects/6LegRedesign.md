---
title: "Passive Energy Saving Robot Leg Design"
collection: projects
permalink: /projects/p6
excerpt: 'Academic Group Project [January 2023 - May 2023]<br/><video src="/images/Leg_Design_Video_0.mp4" controls="controls" style="max-height: 300px;">'
---
[[GitHub]](https://github.com/zixinz990/tmotor_control.git)
* <b>Tech Stack:</b> Python, GitHub, C/C++ 
* <b> Summary </b>
  * Design and build a legged robot that uses springs as a substitute for tendons to store kinetic energy, and develop a control system that can effectively exploit the elastic energy stored in the springs.
  *  Conduct experiments to evaluate the energy efficiency and dynamic performance of the legged robot with different spring configurations, and compare the results with those of a normal two-link leg design, with the goal of providing insights into the design and control of spring-leg systems for more energy-efficient and dynamic legged robots.
  <br><br>
* <b> In-Depth </b>

  * <p style="text-align: justify;"><b>Introduction</b><br>Legged robots have the potential to revolutionize various industries, especially in traversing uneven terrains that are difficult for wheeled robots to navigate. As the configuration and application of legged robots become more complex, they need innovative designs to optimize their performance, especially in terms of energy saving. This project proposes a mechanical add-on inspired by the legs of the ostrich for the legged robots to recover energy. The potential social value of this project lies in the optimization of legged robots' energy efficiency, making them more efficient in traversing uneven terrains, which can have applications in fields such as search and rescue, exploration, and agriculture.</p>
  
  <div style="text-align:center">
    <img src="/images/Leg_Design_1.png" alt="leg" style="width:600px;height:300px;">
  </div>
  <figcaption style="text-align: center;"><u><em>Fig-1 Hypotheses and Expected Energy Transfer (assuming no losses)</em></u></figcaption>
  
  * <p style="text-align: justify;"><b>Electronic System</b><br>Our project aims to optimize the efficiency of legged robots by incorporating a mechanical add-on inspired by the legs of the ostrich to recover energy. To achieve this, we will be using two brushless DC (BLDC) motors, which are known for their durability and efficiency, to drive the leg. The motors will be connected to a Teensy 4.1 microcontroller via a CAN bus module, which will manage the communication logic. The microcontroller will be programmed using the Arduino IDE for faster and simpler programming. Additionally, we will require a PC to provide a 5V voltage and upload codes to Teensy, as well as a power supply to deliver a 24V voltage to the motors. This electronic system design will help us achieve our goal of making legged robots more efficient in traversing uneven terrains.</p>
  
  <div style="text-align:center">
    <img src="/images/Leg_Design_2.png" alt="leg" style="width:600px;height:450px;">
  </div>
  <figcaption style="text-align: center;"><u><em>Fig-2 System Design</em></u></figcaption>
  
  * <p style="text-align: justify;"><b>Control System</b><br>Now to control this system we need to design a controller to controls all the previously introduced electrical components earlier. To start with to detect a jump, we use a contact sensor attached to the end of the leg that activates when the leg touches the ground. Now, to control the position and the state of the leg we have a state estimator that makes sure that the leg always comes back to the same position as the initial position making sure that the robot can jump again.</p>
  
  <div style="text-align:center">
    <img src="/images/Leg_Design_3.png" alt="leg" style="width:600px;height:450px;">
  </div>
  <figcaption style="text-align: center;"><u><em>Fig-3 Controller Design</em></u></figcaption>

  * <p style="text-align: justify;"><b>Experiment</b><br>In order to optimize the efficiency of the jumping movement of the legged robot, the team has designed experiments that incorporate passive dynamics, particularly springs, which are installed between the thigh and calf. Inspired by the tendons of animal legs, the team wants to evaluate the effect of the spring on the robot leg's input efficiency. The robot leg will be fixed onto a track and set to jump to the same height each time, while a weight will be placed on top of the leg to simulate the weight of the springs and the situation in which the robot leg is assembled to a robot dog. The energy consumption of the motor powering the leg will be measured using meters and calculated using equation 1. The team aims to evaluate the efficiency of the leg and will explore other configurations if necessary. The motor is powered by a 24V input, and the team hopes to use a power supply that shows the energy usage over time for more accurate results. </p>
  
  <div style="text-align:center">
    <img src="/images/Leg_Design_4.png" alt="leg" style="width:600px;height:650px;">
  </div>
  <figcaption style="text-align: center;"><u><em>Fig-4 Experimental Setup</em></u></figcaption>
  
  <div style="text-align:center">
    <img src="/images/Leg_Design_5.png" alt="leg" style="width:600px;height:400px;">
  </div>
  <figcaption style="text-align: center;"><u><em>Fig-5 Jumping Height Result</em></u></figcaption>

  * <p style="text-align: justify;">In order to optimize the efficiency of the jumping movement of the legged robot, the team has designed experiments that incorporate passive dynamics, particularly springs, which are installed between the thigh and calf. Inspired by the tendons of animal legs, the team wants to evaluate the effect of the spring on the robot leg's input efficiency. The robot leg will be fixed onto a track and set to jump to the same height each time, while a weight will be placed on top of the leg to simulate the weight of the springs and the situation in which the robot leg is assembled to a robot dog. The energy consumption of the motor powering the leg will be measured using meters and calculating it by finding the total power consumed for the cycle of jumps. The team aims to evaluate the efficiency of the leg and will explore other configurations if necessary. The motor is powered by a 24V input, and the team hopes to use a power supply that shows the energy usage over time for more accurate results. </p>
  
  <div style="text-align:center">
    <video src="/images/Leg_Design_Video.mp4" controls="controls" style="max-width: 700px;"></video>
    </div>
  <figcaption style="text-align: center;"><u><em>Video-1 Leg Jumping</em></u></figcaption>
  
  * <p style="text-align: justify;"><b>Result</b><br>The team was conclusively able to prove out initial hypothesis right. Also, the future work would include utilizing different springs and different orientation to study the impact of position and hooks-law on efficiency improvement.</p>