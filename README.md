# Human-aware Design Generation: Adding 3D Humans into Graphic Designs

Official repository for **Human-aware Design Generation: Adding 3D Humans into Graphic Designs**.

> **Code and model weights coming soon.**

## Overview

Graphic designs frequently contain human images whose pose, framing, and placement are carefully designed to guide visual exploration and evoke particular feelings. Existing automatic graphic-design generation methods have largely overlooked the role of human representations in the design process.

We introduce **design-conditioned 3D human adding**, a task that adds a 3D human representation to an existing partial graphic design. Given a design containing elements such as images, vector shapes, and text, our model predicts:

- the 3D pose of the human;
- the 2D framing of the human image; and
- the spatial layout of the image containing the human within the design.

The predicted human and image layout are then integrated with the existing design elements to produce a cohesive complete design. Our experiments show improvements over baseline methods in 3D pose prediction, 2D framing, image layout harmonization, and holistic design quality.

## Visual Results

Click any image to open the full-resolution figure.

### Task Overview

<p align="center">
  <a href="https://raw.githubusercontent.com/GreyNails/Human-aware-Design-Generation-Adding-3D-Humans-into-Graphic-Designs/main/figure/fig1_teaser.png"><img src="https://raw.githubusercontent.com/GreyNails/Human-aware-Design-Generation-Adding-3D-Humans-into-Graphic-Designs/main/figure/fig1_teaser.png" alt="Overview of design-conditioned 3D human adding" width="85%"></a>
</p>

Given an input design (1st column) with a set of elements such as images, vector shapes and texts, our model adds a 3D human into the design (2nd column) by predicting its 3D pose, 2D framing, and the layout of the image containing the human. The result is a cohesive output design with the 3D human added (3rd column), which can further be rendered into a realistic human image (4th column).

### Model Overview

<p align="center">
  <a href="https://raw.githubusercontent.com/GreyNails/Human-aware-Design-Generation-Adding-3D-Humans-into-Graphic-Designs/main/figure/fig3_model.png"><img src="https://raw.githubusercontent.com/GreyNails/Human-aware-Design-Generation-Adding-3D-Humans-into-Graphic-Designs/main/figure/fig3_model.png" alt="Model overview" width="85%"></a>
</p>

Our model takes a partial graphic design with multimodal elements (images, texts, vector shapes) and generates a complete design with one or several 3D humans. An encoder extracts element-wise embeddings, which feed a pose-and-framing generator and a layout generator. The pose-and-framing generator autoregressively produces pose tokens (decoded into 3D poses by a pre-trained decoder) and framing tokens that control composition, while the layout generator predicts the bounding box and z-order of the human image in the design.

### Qualitative Comparison

<p align="center">
  <a href="https://raw.githubusercontent.com/GreyNails/Human-aware-Design-Generation-Adding-3D-Humans-into-Graphic-Designs/main/figure/fig4_comparison.png"><img src="https://raw.githubusercontent.com/GreyNails/Human-aware-Design-Generation-Adding-3D-Humans-into-Graphic-Designs/main/figure/fig4_comparison.png" alt="Qualitative comparison" width="85%"></a>
</p>

Qualitative comparison of different methods. Our approach predicts 3D poses, 2D framing and human-image layouts that harmonize better with the existing design elements and produce higher-quality holistic designs.

### Realistic Rendering

<p align="center">
  <a href="https://raw.githubusercontent.com/GreyNails/Human-aware-Design-Generation-Adding-3D-Humans-into-Graphic-Designs/main/figure/fig5_rendering.png"><img src="https://raw.githubusercontent.com/GreyNails/Human-aware-Design-Generation-Adding-3D-Humans-into-Graphic-Designs/main/figure/fig5_rendering.png" alt="Realistic rendering results" width="85%"></a>
</p>

Results of different methods where the added 3D humans are rendered into realistic human images, showing that our predicted representations integrate naturally into the final designs.

## Status

This repository provides the paper figures and project overview.

- [ ] Inference code
- [ ] Training code
- [ ] Pre-trained model weights
- [ ] Dataset and data-processing instructions
- [ ] Detailed installation and evaluation instructions

All of the above will be released soon.

## Repository Structure

```text
.
├── figure/              # Paper figures and visual results
└── README.md
```

## Paper

**Human-aware Design Generation: Adding 3D Humans into Graphic Designs**  
Zijin Hou and Ying Cao  
ShanghaiTech University

Published in the *Proceedings of the 34th ACM International Conference on Multimedia (MM 2026)*.

- DOI: [10.1145/3767308.3836019](https://doi.org/10.1145/3767308.3836019)
- Paper/project materials: coming soon

## Citation

The BibTeX citation will be added when the final publication metadata is available.

```bibtex
@inproceedings{hou2026humanaware,
  title     = {Human-aware Design Generation: Adding 3D Humans into Graphic Designs},
  author    = {Hou, Zijin and Cao, Ying},
  booktitle = {Proceedings of the 34th ACM International Conference on Multimedia},
  year      = {2026},
  doi       = {10.1145/3767308.3836019}
}
```

## License

The license for the code, model weights, and associated materials will be specified when they are released.

## Contact

For questions, please contact:

- Zijin Hou: houzj2025@shanghaitech.edu.cn
- Ying Cao: caoying59@gmail.com
