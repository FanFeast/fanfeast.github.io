---
title: "CutScene: Active Vision for Next Best View Planning"
collection: projects
excerpt: '(CMU 16824 Course Project [January 2023 - May 2023]) <a href="https://github.com/FanFeast/NeU-NBV-prediction.git" target="_blank">Visit Project</a><br/><video src="/images/CutScene-Augmentation.gif" controls="controls" style="max-height: 300px;">Your browser does not support the video tag.</video>'
---

## Overview

**CutScene** is an academic group project developed as part of CMU's 16824 Visual Learning course, focusing on active vision for Next Best View (NBV) Planning in outdoor scenes. This project extends the NeU-NBV framework to larger outdoor navigational environments using a novel data augmentation technique.

**Team Members:** [Aditya Rauniyar](https://adityarauniyar.com/), [Omar Alama](https://www.linkedin.com/in/omaralama/), [Yuechuan Hou](https://yuechuanhou.com/), [Mukul Ganwal](https://www.linkedin.com/in/mukul-ganwal/)

**Institution:** Carnegie Mellon University
**Duration:** January 2023 - May 2023

---

## Abstract

This project addresses autonomous robotic tasks in large-scale outdoor scenes by extending next best view planning capabilities. We introduce a **cutscene augmentation method** that semantically divides larger outdoor scenes into smaller components, significantly improving training efficiency and prediction accuracy. Our model is trained to predict uncertainty and RGB values for novel poses within segmented scenes, enabling more effective data collection strategies for outdoor navigation scenarios.

## Key Contributions

### 1. **Training on Larger Outdoor Scenes**
- Utilized the UrbanScene3D dataset for large-scale outdoor environments
- Imported 3D scene representations into Blender
- Generated custom datasets emulating DTU dataset configuration with camera poses and renders

### 2. **Viewing Range Sensitivity Analysis**
- Conducted comprehensive analysis across multiple viewing angles (30°, 60°, 90°)
- Created datasets with double dome configurations
- Evaluated the impact of viewing range on reconstruction quality and uncertainty estimation
- Demonstrated high sensitivity of the framework to viewing range parameters

### 3. **Cutscene Augmentation (Novel Technique)**
Inspired by 2D augmentation methods like cutout and cutmix, we developed **cutscene augmentation** which:
- Semantically divides large outdoor scenes into smaller subscenes
- Increases dataset size and variation significantly
- Reduces overfitting when training data is scarce
- Substantially improves novel view prediction accuracy
- Enhances the network's generalization capabilities

## Technical Approach

### Foundation
Built upon the [NeU-NBV framework](https://arxiv.org/abs/2303.01284) by Jin et al., which adapts PixelNeRF for next best view planning using:
- LSTM-based ray tracing optimization for faster volumetric rendering
- Uncertainty estimation through log-normal distribution sampling
- Information gain maximization for view selection

### Architecture
- **Network:** Modified PixelNeRF with uncertainty prediction
- **Loss Function:** Uncertainty-guided loss for RGB and variance prediction
- **Planning Framework:** Iterative next best view selection based on pixel uncertainty

### Training Setup
- **Hardware:** NVIDIA 3090Ti GPU
- **Epochs:** 200
- **Dataset:** UrbanScene3D with custom Blender rendering pipeline
- **Metrics:** PSNR and SSIM for reconstruction quality evaluation

## Results

### Viewing Range Analysis
- Demonstrated clear trade-off between viewing range and reconstruction quality
- Smaller viewing ranges (30°) achieved superior PSNR and SSIM scores
- Uncertainty predictions correlated well with error across all viewing ranges
- Validated the framework's sensitivity to viewing angle parameters

### Cutscene Augmentation Impact
- **Significant performance improvements** over baseline models
- Successfully generalized to broader viewing ranges (90°) despite training on 60° data
- Surpassed DTU pretrained baseline on outdoor scenes
- Reduced uncertainty noise, improving NBV planning reliability
- Clear visual improvements in both RGB reconstruction and uncertainty estimation

### Next Best View Planning
Compared three policies:
1. **Our Method** (Cutscene + Uncertainty-guided)
2. **DTU Baseline** (Pretrained model)
3. **Maximum View Distance** (Geometric baseline)

Our approach **outperformed both baselines** in reconstruction quality as measured by PSNR and SSIM metrics across iterative view collection.

## Future Directions

1. **Automated Semantic Division:** Utilize 2D bird's eye view detectors or geometric clustering for automatic scene segmentation
2. **Scene Rearrangement:** Extend augmentation by creating novel configurations from cutout scenes
3. **Scheduled Viewing Range:** Implement gradual viewing range increase during training for better stability and generalization
4. **Multi-UAV Integration:** Explore collaborative data collection strategies

## Technologies & Methods

- **Deep Learning:** NeRF, PixelNeRF, Neural Radiance Fields
- **Computer Vision:** Novel view synthesis, uncertainty estimation, active vision
- **3D Reconstruction:** Volumetric rendering, ray tracing optimization
- **Tools:** Blender, Python, PyTorch
- **Datasets:** UrbanScene3D, DTU (for comparison)

## Impact

This work successfully demonstrates the extension of indoor-focused next best view planning methods to large-scale outdoor environments, addressing key challenges in autonomous navigation and robotic exploration. The cutscene augmentation technique provides a practical solution for dealing with scarce large-scale outdoor training data.

---

**Project Website:** [adityarauniyar.com/cutscene.github.io](https://github.com/FanFeast/NeU-NBV-prediction.git)

**Citation:**
```bibtex
@article{2023cutscene,
  title={Cutscene: Active vision for Next Best View Planning in outdoor scenes},
  author={Rauniyar, Aditya and Alama, Omar and Hou, Yuechuan and Ganwal, Mukul},
  url={https://github.com/FanFeast/NeU-NBV-prediction.git},
  year={2023}
}
```
