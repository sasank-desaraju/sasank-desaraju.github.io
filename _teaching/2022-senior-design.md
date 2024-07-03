---
title: "Supervised CS Senior Design group (Spring 2022)"
collection: teaching
type: "Graduate course"
permalink: /teaching/2022-senior-design
venue: "University of Florida, Department of Mechanical Engineering, Banks Lab"
date: 2022-01-15
location: "Gainesville, Florida"
---

I supervised a group of undergraduate computer science students in their senior design project.
I led the 4 students in a project that used AI to create realistic images of bone X-rays.
More specifically, we used Generative Adversarial Networks (GANs) to reconstruct X-rays of canine legs in specific positions.

Our goal was to create realistic X-ray images that could be used in a larger project in the lab that was trying to identify bone position from X-ray images.
In order for this larger project to have more robust training data, we need to create an "X-ray" from a specific bone position.
Ray-tracing 3D bone models can render the position of the bones, but misses the many artifacts introduced by soft tissue, cortical distribution bone density, and other sources.
The discrepancy between ray-traced images and true X-rays was significat to the larger position estimation projects, and we hoped to mimic these artifacts using GAN image reconstruction.
We used a style transfer model to translate from a point cloud representation of bone models to an X-ray-like image.

We succeeded in producing images that accurately represented bone position and included some artifacts.
However, more work is needed to sufficiently realistic images.
Future work may use more advanced methods, such as diffusion methods.
Alternatively, one could accelerate voxel-based bone model rendering so that some artifacts, such as the distribution of bone density, is rendered accurately.
