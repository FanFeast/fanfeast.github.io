---
permalink: /
title: "BIOGRAPHY"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi, I'm **Mukul Ganwal** - a passionate roboticist driven by my love for robots and their potential to transform our world. 

Here's my [Curriculum Vitae](https://drive.google.com/file/d/1zffJzrKkVPekjVyz5iA-gMLBF_hO8kBR/view?usp=sharing) for detailed information.

I am a Senior Perception Engineer and Team Lead at Anyware Robotics, where I rebuilt and grew the perception team to 5 engineers and own the roadmap across 3D perception, camera systems, and learning-based work. My work focuses on building production-grade machine learning pipelines that enable robots to understand and interact with complex real-world environments. I ship systems that use three RGB-D cameras to reconstruct work cells in 0.1 seconds, allowing FANUC CRX25 robots to palletize boxes in 6.3 seconds each at 573 boxes/hour.

Most recently, I architected a custom dual-head, NMS-free segmentation model end-to-end — adding a wireframe pose-detection head that enables direct 3D box pose estimation — reaching 99.4 mAP@50 while cutting inference from 56 ms to 7 ms. I also overhauled the 2D/3D perception pipeline, parallelizing preprocessing across three cameras and refactoring the point-cloud stack to cut 2D compute from 900 ms to 90 ms and 3D from 2 s to 300 ms; hiding perception behind arm motion brought the pick cycle from 12 s down to 9 s and lifted throughput by 100+ cases/hour. I'm also a co-inventor on a U.S. provisional patent for multi-purpose robotic systems for warehouse automation.

My expertise lies at the intersection of robotics, computer vision, and MLOps. I specialize in creating active-learning workflows that dramatically reduce data labeling requirements - achieving 40% reductions in manual annotation while maintaining rapid 40-minute test-to-deploy cycles. I've pioneered the use of synthetic data generation through Blender photogrammetry combined with StyleGAN3 domain randomization, scaling datasets by 8× and improving detection performance by 4.7 percentage points. My systems integrate seamlessly with ROS 2 architectures, incorporating behavior trees and hierarchical finite-state machines with real-time fault classification that has reduced unplanned robot downtime by 35%.

Before joining Anyware Robotics, I honed my skills as a Graduate Research Assistant at the BioRobotics Lab in Pennsylvania, where I engineered modular battery extraction mechanisms for Apple devices and built real-time multi-class instance segmentation pipelines achieving 98% accuracy. My journey into robotics and AI began with internships at PGP Glass and other companies, where I developed visual inspection systems with 99% defect detection accuracy and created intelligence systems that transformed business operations.

My technical toolkit spans **PyTorch, JAX, ONNX, TensorRT, CUDA, OpenCV, Open3D, PCL, and ROS/ROS2** for ML, perception, and robotics, complemented by **Docker, Kubernetes, Ray, Git, AWS, and GCP** for robust MLOps deployments. I'm proficient in **Python, C/C++, MATLAB, and Bash** across **Ubuntu LTS/Pro RT and FreeRTOS** environments, with expertise in simulation platforms like **Isaac Sim, Gazebo, and PyBullet** alongside CAD tools like **SolidWorks**.

What drives me is the belief that robots can fundamentally improve how we work and live. Every system I build bridges the gap between cutting-edge AI research and practical robotic applications that deliver measurable impact in real manufacturing environments.

*"My heart in my work" - Andrew Carnegie*
