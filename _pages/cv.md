---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

# Education
* M.D.-Ph.D. Candidate, University of Florida, 2029 Ph.D., 2031 M.D. (expected)
* M.S. in Biomedical Engineering, University of Florida, 2023
* B.S. in Physics, University of Florida, 2021
* B.A. in Mathematics, University of Florida, 2021

<!-- _GD GPA:_ **4.00** &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; _UG GPA:_ **3.92** &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; _MCAT:_ **525** (100th Pctl.) &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; _GRE:_ **166**(V), **170** (Q) -->

<div style="display: flex; justify-content: space-between;">
  <span><em>GD GPA:</em> <strong>4.00</strong></span>
  <span><em>UG GPA:</em> <strong>3.92</strong></span>
  <span><em>MCAT:</em> <strong>525</strong> (100th Pctl.)</span>
  <span><em>GRE:</em> <strong>166</strong>(V), <strong>170</strong> (Q)</span>
</div>


# Experience

- <div style="display: flex; justify-content: space-between; width: 100%;">
    <span>AI reconstruction of surgical images to improve safety</span>
    <span>(Fall 2021-Current)</span>
  </div>
  - Created AI model to highlight common bile duct during laparoscopic cholecystectomy surgery
  - Implemented pipeline using CycleGAN for image-to-image translation from whitelight imaging to fluorescent imaging

- <div style="display: flex; justify-content: space-between; width: 100%;">
    <span>Autonomous Joint Tracking on Native Knees (Master's thesis project)</span>
    <span>(Fall 2021-Summer 2023)</span>
  </div>
  - Created a deep learning-based system to predict joint kinematics in native (no implant) knee joints
  - We used canine stifle (knee joint) images taken during treadmill walking fluoroscopy trials
  - I implemented a keypoint estimator deep neural network using ResNet with PyTorch Lightning, trained on HiPerGator, UF's supercomputer

- <div style="display: flex; justify-content: space-between; width: 100%;">
    <span>Segmentation of enteric fistulae</span>
    <span>(Fall 2022-Summer 2023)</span>
  </div>
  - Created MONAI deep learning pipeline to segment small abdominal fistulae from patients with Crohn's Disease

# Skills
- Computer Vision with PyTorch, PyTorch Lightning
- HPC, SLURM, SSH, Containers
    - I use UF's supercomputer, HiPerGator, which uses SLURM
    - HiPerGator uses Apptainer/Singularity containers, which are similar to Docker
- Linux, NeoVim, Tmux
- R, RStudio

# Publications
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
# Talks
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
# Teaching
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
# Service and leadership
- Medical Artificial Intelligence Interest Group (MAIIG), UF College of Medicine, President
- American Physician Scientist Association (APSA), UF College of Medicine, President

# Hobbies
- Rubik's cube solving
    - I currently average under 20 seconds for the normal 3x3 and went to a few [competitions](https://www.worldcubeassociation.org/persons/2016DESA03) in the past.
