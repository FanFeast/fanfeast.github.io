---
title: "Lunar Rover Landing Site Analysis & Path Planner"
collection: projects
permalink: /projects/p4
excerpt: 'Group Project [September 2022 - December 2022]'
---

[[ppt]](https://docs.google.com/presentation/d/14eA6XsbJ2c8gRGJ7MdhdhHJT0oORI3D_/edit?usp=sharing&ouid=114350528429388663351&rtpof=true&sd=true)[[code]](https://github.com/FanFeast/Landing_Site_Navigation_and_Path_Planning)


* <b>Tech Stack:</b> C/C++ (Eigen3, Embree 3.0, fmt), GitHub 
  <br>
  <figure style="text-align:center;">
    <img src="/images/Lunar_project_pit_3d.png" alt="PIT" style="width:500px;height:300px;">
  </figure>
  <figcaption style="text-align: center;"><u><em>Fig-1 3D Render of Lacus Mortis Pit</em></u></figcaption>
  <br>
  * <p style="text-align: justify;">The following project was conducted in collaboration with Planerty Labs at CMU as part of a larger project aimed at exploring the Lunar surface,     particularly low-light zones like the pits. These areas cannot be observed by cameras from satellites orbiting the moon, and sending the rover to explore   them is not an option as the rover must maintain a line of sight with the lander (as explained in Fig-2) at all times to transmit information such as photos  and samples. Therefore, an algorithm was developed to find the optimal landing site and generate an optimal path for the rover to travel. The needed input  for the algorithm is a 3D render of the landign surface (as shown in Fig-1).</p>
  <br>
  <div style="display: flex; flex-direction: row; justify-content: center; align-items: center;">
    <div style="width: 50%; text-align: center;">
      <img src="/images/Lunar_project_LOS1.png" style="width: 100%;" />
    </div>
    <div style="width: 50%; text-align: center;">
      <img src="/images/Lunar_project_LOS2.png" style="width: 100%;" />
    </div>
  </div>
  <figcaption style="text-align: center;"><em><u>Fig-2 Line of Sight of Rover</u></em></figcaption>
  <br>
  <br>
  * <p style="text-align: justify;">The project aimed to use a 3D render of the surface of the Moon to generate a depth map of the surface. To achieve this, the project utilized ray tracing, a technique used in computer graphics to simulate the path of light rays as they interact with objects in a scene. By using ray tracing to render the surface of the moon, the project was able to calculate the distance between the camera (or the observer) and each point on the surface, which allowed for the generation of a depth map. This depth map then enabled the project to generate a slope map and a Line of Sight (LOS) map. Ray tracing was used in this project to render a 3D model of the lunar surface and obtain depth information that was essential in generating the slope and LOS maps, as well as identifying optimal landing sites and paths for the rover.The depth map was then used to generate a slope map, where darker shades represented higher slopes or inaccessibility. The rover had physical constraints such as maintaining a line of sight with the lander, slope constraints, and distance constraints. The landing site needed to be evaluated based on these parameters. The algorithm was developed to identify the best landing site and the most optimal path for the rover to explore. The algorithm emplyed a complex G-Score funciton to evaluate all possible landing sites and find the optimal path for the rover to travel.</p>

  <figure style="text-align:center;">
    <img src="/images/Lunar_project_output.png" alt="output" style="width:500px;height:250px;">
  </figure>

  <figcaption style="text-align: center;"><em><u>Fig-3 Line of Sight of Rover</u></em></figcaption>

  <br><br>
  * <p style="text-align: justify;">The Line of Sight Map (LOS Map) was generated to represent all the points on the map where the lander could communicate with the rover, and a LOS Aggregate Map was also created to ensure the landing site covered the entire pit in its line of sight. This had to be done becuase the lander could land anywhere in the targereted landing circle and due to that there could be numerious posiibility based on where the lander lands on the circle. Hence, we generate the LOS Aggregate Map to make sure we are considering all the different possibilites. These can be seen in Fig-3 and Fig-5 where the different intensity of Green shows the Coverage of the paticialr points based on different landing locations in the circle. For accomlishing the true purpose of the project of exploring the pits on the lunar surface thirty-six sites called vantage points were generated around the pit space at 10-degree intervals from the center of the pit, and the optimal sites were determined by overlaying the LOS map. A complex G-score function was created to assign penalties to different parameters and generate a ranking to select the best path.</p>

  <figure style="text-align:center;">
    <img src="/images/Lunar_project_Vantage_Point_generation.png" alt="Vantage Point Generation" style="width:500px;height:200px;">
  </figure>

  <figcaption style="text-align: center;"><u><em>Fig-4 Vantage poitns are generated based on where the meet the LOS coverage and the Pits border</em></u></figcaption>
     
  <br>
  * <p style="text-align: justify;">In Fig-5 you can see the algorithm going through different possible landing sites and evaluating which is the best landing site for the rover.</p> 
  <br><br>
  
  <figure style="text-align:center;">
    <img src="/images/Lunar_project_Site_Evaluator_Working.gif" alt="Working" style="width:400px;height:400px;">
  </figure>

  <figcaption style="text-align: center;"><u><em>Fig-5 Algorithm going though various landing sites (blue circle) and the 
    correspoing changes in the LOS Map (Green Shade) based on the Depth Map (Red Shades)</em></u></figcaption>
    
  <br><br>
  * <p style="text-align: justify;">The results of the project were successful, with an algorithm that was able to find a list of the best landing sites and generated an optimal path for the rover to traverse around the Lacus Mortis Pit. The code gengerated has also been done in a very modular way and can be used to generatea paths and best landing sites by altering the G-Score funcstion based on the requirements. Also, an overlay extension (called mapWindow) was also created, allowing the generated path to be overlaid with the actual image from the Moon, making it easier to visualize and justify.</p>

  <figure style="text-align:center;">
    <img src="/images/Lunar_project_overlay.png" alt="Overlay" style="width:400px;height:400px;">
  </figure>
  <figcaption style="text-align: center;"><u><em>Fig-6 Currently shows the Generated Path and Satellite Image Overlay</em></u></figcaption>
