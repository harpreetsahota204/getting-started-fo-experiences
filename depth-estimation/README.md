# Getting Started with Depth Estimation

## Depth Data Loading Examples

This demonstrates how to load and visualize depth estimation datasets using FiftyOne. Examples include:

### DIODE Dataset
- Loads depth maps from NumPy arrays (.npy files)
- Handles depth masks for valid measurements
- Visualizes depth data as heatmaps with appropriate ranges

### NYU Depth V2 Dataset  
- Loads depth maps from PNG image files
- Organizes data by room type and scene
- Groups frames to enable video-like visualization

### CLEVR Dataset
- Simple synthetic dataset with 3D rendered objects
- RGB images paired with Marigold-generated depth maps
- Depth maps stored as PNG files in parallel directory structure
- Visualizes predicted depth as heatmaps in FiftyOne
- Useful for evaluating depth estimation models on clean, controlled scenes

## Depth Estimation with FiftyOne

This repository demonstrates different approaches to running depth estimation models using FiftyOne. The notebook covers:

### Dataset Preparation
- Loading CLEVR dataset from Hugging Face Hub
- Converting to FiftyOne format with proper depth map visualization
- Organizing RGB-depth pairs with metadata

### Depth Estimation Methods

#### FiftyOne Zoo Models
- Direct integration with Hugging Face transformers
- Support for models like:
  - Depth Anything V2
  - Intel DPT models
  - ZoeDepth
  - GLPN
- Simple API for model loading and inference

#### Custom Model Integration 
- Manual implementation for non-Zoo compatible models
- Example using DPT-BEiT model
- Proper handling of model outputs and visualization

#### Community Plugins
- Integration with DepthPro plugin
- Delegated processing support
- Multiple depth estimation types

#### Diffusers
- Using Marigold depth estimation pipeline
- Saving depth maps alongside source images
- Both visualization and 16-bit depth map export


# Citations

### Datasets

##### DIODE Dataset

```bibtex
@article{diode_dataset,
  title={{DIODE}: {A} {D}ense {I}ndoor and {O}utdoor {DE}pth {D}ataset},
  author={Igor Vasiljevic and Nick Kolkin and Shanyi Zhang and Ruotian Luo and
  Haochen Wang and Falcon Z. Dai and Andrea F. Daniele and Mohammadreza Mostajabi and
  Steven Basart and Matthew R. Walter and Gregory Shakhnarovich},
  journal={CoRR},
  volume={abs/1908.00463},
  year={2019},
  url={http://arxiv.org/abs/1908.00463}
}
```

##### NYUv2 Depth Dataset

```bibtex
@inproceedings{Silberman:ECCV12,
  author    = {Nathan Silberman, Derek Hoiem, Pushmeet Kohli and Rob Fergus},
  title     = {Indoor Segmentation and Support Inference from RGBD Images},
  booktitle = {ECCV},
  year      = {2012}
}
```

##### CLEVR Depth Dataset

```bibtex
@inproceedings{johnson2017clevr,
  title = {CLEVR: A Diagnostic Dataset for Compositional Language and Elementary Visual Reasoning},
  author = {Johnson, Justin and Hariharan, Bharath and van der Maaten, Laurens and Fei-Fei, Li and Zitnick, C. Lawrence and Girshick, Ross},
  booktitle = {Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition},
  year = {2017}
}
```


### Models

##### Depth Anything V2

```bibtex
@article{depth_anything_v2,
  title={Depth Anything V2},
  author={Yang, Lihe and Kang, Bingyi and Huang, Zilong and Zhao, Zhen and Xu, Xiaogang and Feng, Jiashi and Zhao, Hengshuang},
  journal={arXiv:2406.09414},
  year={2024}
}

@inproceedings{depth_anything_v1,
  title={Depth Anything: Unleashing the Power of Large-Scale Unlabeled Data}, 
  author={Yang, Lihe and Kang, Bingyi and Huang, Zilong and Xu, Xiaogang and Feng, Jiashi and Zhao, Hengshuang},
  booktitle={CVPR},
  year={2024}
}
```

##### Intel DPT

```bibtex
@article{DBLP:journals/corr/abs-2103-13413,
  author    = {Ren{\'{e}} Reiner Birkl, Diana Wofk, Matthias Muller},
  title     = {MiDaS v3.1 – A Model Zoo for Robust Monocular Relative Depth Estimation},
  journal   = {CoRR},
  volume    = {abs/2307.14460},
  year      = {2021},
  url       = {https://arxiv.org/abs/2307.14460},
  eprinttype = {arXiv},
  eprint    = {2307.14460},
  timestamp = {Wed, 26 Jul 2023},
  biburl    = {https://dblp.org/rec/journals/corr/abs-2307.14460.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```

##### DepthPro

```bibtex
@article{Bochkovskii2024:arxiv,
  author     = {Aleksei Bochkovskii and Ama\"{e}l Delaunoy and Hugo Germain and Marcel Santos and
               Yichao Zhou and Stephan R. Richter and Vladlen Koltun}
  title      = {Depth Pro: Sharp Monocular Metric Depth in Less Than a Second},
  journal    = {arXiv},
  year       = {2024},
  url        = {https://arxiv.org/abs/2410.02073},
}
```

##### Marigold

```bibtex
@InProceedings{ke2023repurposing,
      title={Repurposing Diffusion-Based Image Generators for Monocular Depth Estimation},
      author={Bingxin Ke and Anton Obukhov and Shengyu Huang and Nando Metzger and Rodrigo Caye Daudt and Konrad Schindler},
      booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
      year={2024}
}
```