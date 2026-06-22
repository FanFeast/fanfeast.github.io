---
layout: archive
title: "Industry Experience"
permalink: /industry-experience/
author_profile: true
---

{% include base_path %}

<style>
  .experience-section {
    display: flex;
    align-items: flex-start;
    margin-bottom: 2rem;
  }

  .experience-section img {
    width: 250px;
    height: auto; /* Maintain aspect ratio */
    margin-left: 1.5rem; /* Add space between image and text */
  }

  .experience-text {
    max-width: 70%; /* Limit the text width for better readability */
  }

  .experience-text a {
    text-decoration: none;
    color: inherit;
  }

  .experience-text a:hover {
    text-decoration: underline;
  }
</style>

---

<div class="experience-section">
  <div class="experience-text">
    <h2><a href="https://anywarerobotics.com" target="_blank">Anyware Robotics</a></h2>
    <strong>Senior Perception Engineer (Team Lead)</strong> [Jan 2026 – Present]  
    <ul>
      <li>Rebuilt and grew the perception team to 5 engineers; own project scope and roadmap across 3D perception, camera systems, and learning-based work, with day-to-day technical mentorship.</li>
      <li>Architected a custom dual-head, NMS-free segmentation model end-to-end, adding a wireframe pose-detection head for direct 3D box pose estimation — achieving 99.4 mAP@50 (+1.7 pp) and 98.7 mAP@50–95 (+2.4 pp) while cutting inference from 56 ms to 7 ms.</li>
      <li>Overhauled the 2D/3D perception pipeline (parallelized 3-camera preprocessing, GPU-accelerated segmentation, refactored point-cloud stack), cutting 2D compute 900 ms → 90 ms and 3D 2 s → 300 ms; hid perception behind arm motion to bring the pick cycle from 12 s to 9 s and lift throughput by 100+ cases/hour.</li>
    </ul>
    <strong>Perception Engineer II</strong> [Jan 2024 – Dec 2025]  
    <ul>
      <li>Shipped an end-to-end palletizing perception stack: three RGB-D cameras reconstruct the work cell in 0.1 s, enabling a FANUC CRX25 to palletize boxes in 6.3 s each at 573 boxes/hour.</li>
      <li>Built an active-learning MLOps workflow with ensemble uncertainty scoring using foundation models for zero-shot labeling via Label Studio on GCP & Ray — reducing manual annotation by 40% and test-to-deploy cycles to 40 minutes.</li>
      <li>Scaled training data via synthetic generation: Blender photogrammetry + StyleGAN3 domain randomization (21 styles) expanded the dataset 8× and improved detection mAP by +4.7 pp.</li>
      <li>Deployed optimized models with ONNX + TensorRT on GPU edge devices for real-time inference, and orchestrated a ROS 2 Humble behavior-tree and HFSM control stack with real-time fault classifiers, reducing unplanned robot downtime by 35% across pilot cells.</li>
    </ul>
  </div>
  <img src="/images/AWR_Logo.png" alt="Anyware Robotics Logo">
</div>

---

<div class="experience-section">
  <div class="experience-text">
    <h2><a href="https://www.google.com">PGP Glass Private Limited</a></h2>
    <strong>Data Science Intern</strong> [July 2022 - August 2022]  
    <ul>
      <li><strong>Tech Stack:</strong> Catia, SolidWorks, Coppelia Sims (V-Rep Simulator), Python (PyBullet), C/C++.</li>
      <li>Deployed a quality control automation system for glass defect detection.</li>
      <li>Created Python scripts to generate intelligence reports from export databases.</li>
    </ul>
  </div>
  <img src="/images/PGP_Logo.png" alt="PGP LOGO">
</div>

---

<div class="experience-section">
  <div class="experience-text">
    <h2><a href="https://www.google.com">Maruti Suzuki Private Limited</a></h2>
    <strong>Data Science Intern</strong> [January 2022 - June 2022]  
    <ul>
      <li><strong>Tech Stack:</strong> Python (PySpark, PyTorch), C/C++, Congos, PowerBI, AWS, Git, IBM-Cp4d.</li>
      <li>Enhanced preprocessing pipeline with PySpark, improving speed and efficiency.</li>
      <li>Built a database for electric vehicle charging station locations.</li>
      <li>Developed a warning system for vehicle failure prediction.</li>
    </ul>
  </div>
  <img src="/images/MS_Logo.png" alt="Maruti LOGO">
</div>

---

<div class="experience-section">
  <div class="experience-text">
    <h2><a href="https://www.google.com">Hero Motor Corp</a></h2>
    <strong>Summer Intern</strong> [July 2021 - August 2021]  
    <ul>
      <li><strong>Tech Stack:</strong> Python, MS Office.</li>
      <li>Designed packaging labels in compliance with the Packaging Commodity Act.</li>
      <li>Conducted packaging data analysis and error detection using Python.</li>
    </ul>
  </div>
  <img src="/images/Hero_Logo.png" alt="Hero LOGO">
</div>
