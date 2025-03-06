# Getting Started with Depth Estimation

# Depth Data Loading Examples

This demonstrates how to load and visualize depth estimation datasets using FiftyOne. Examples include:

## DIODE Dataset
- Loads depth maps from NumPy arrays (.npy files)
- Handles depth masks for valid measurements
- Visualizes depth data as heatmaps with appropriate ranges

## NYU Depth V2 Dataset  
- Loads depth maps from PNG image files
- Organizes data by room type and scene
- Groups frames to enable video-like visualization


# Monocular Depth Estimation



# Citations

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

```bibtex
@inproceedings{Silberman:ECCV12,
  author    = {Nathan Silberman, Derek Hoiem, Pushmeet Kohli and Rob Fergus},
  title     = {Indoor Segmentation and Support Inference from RGBD Images},
  booktitle = {ECCV},
  year      = {2012}
}

@inproceedings{icra_2019_fastdepth,
    author      = {{Wofk, Diana and Ma, Fangchang and Yang, Tien-Ju and Karaman, Sertac and Sze, Vivienne}},
    title       = {{FastDepth: Fast Monocular Depth Estimation on Embedded Systems}},
    booktitle   = {{IEEE International Conference on Robotics and Automation (ICRA)}},
    year        = {{2019}}
}
```