---
title: "Lunar Rover Landing Site Analysis & Path Planner"
collection: projects
permalink: /projects/p1
excerpt: 'Independent Group Project [September 2022]'
---

* <b>Tech Stack:</b> C/C++, GitHub
[[ppt]](https://docs.google.com/presentation/d/14eA6XsbJ2c8gRGJ7MdhdhHJT0oORI3D_/edit?usp=sharing&ouid=114350528429388663351&rtpof=true&sd=true)[[code]](https://github.com/FanFeast/Engineering_Computation)

<p>The following project was conducted in collaboration with Planerty Labs at CMU as part of a larger project aimed at exploring the Lunar surface, particularly low-light zones like the pits. These areas cannot be observed by cameras from satellites orbiting the moon, and sending the rover to explore them is not an option as the rover must maintain a line of sight with the lander at all times to transmit information such as photos and samples. Therefore, an algorithm was developed to find the optimal landing site and generate an optimal path for the rover to travel.</p>

<center><figure>
  <img src="/images/Lunar_project_pit_3d.png" alt="Working" style="width:400px;height:400px;">
  </figure></center>


<p>The project involved generating a 3D render of the Lunar surface and using it to create a depth map, which was then used to generate a slope map in red color gradient to indicate areas with higher slopes or inaccessibility. The rover also had physical constraints, including line of sight with the lander at all times, slope constraints, and distance constraints, which were all taken into account during the algorithm's development. The algorithm employed C++ and A-Star Algorithm to evaluate all possible landing sites and find the optimal path for the rover to travel.</p>
<center><figure>
  <img src="/images/Lunar_project_Site_Evaluator_Working.gif" alt="Working" style="width:400px;height:400px;">
  </figure></center>

<p>The Line of Sight Map (LOS Map) was generated to represent all the points on the map where the lander could communicate with the rover, and an LOS Aggregate Map was also created to ensure the landing site covered the entire pit in its line of sight. Thirty-six sites were generated around the pit space at 10-degree intervals from the center of the pit, and the optimal sites were determined by overlaying the LOS map. A complex G score function was used to assign penalties to different parameters and generate a ranking to select the best path.</p>

<center><figure>
  <img src="/images/Lunar_project_output.png" alt="output" style="width:500px;height:200px;">
  </figure></center>


<p>The results of the project were successful, with an algorithm that found the best landing site and generated an optimal path for the rover. An overlay extension was also created, allowing the generated path to be overlaid with the actual image from the Moon, making it easier to visualize and justify.</p>

<center><figure>
  <img src="/images/Lunar_project_Site_Evaluator_Working.gif" alt="Overlay" style="width:400px;height:400px;">
 </figure></center>

