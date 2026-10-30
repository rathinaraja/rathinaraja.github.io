---
layout: page
title: Projects
permalink: /projects/
description:
nav: true
nav_order: 2
---

<style>
.research-projects{max-width:1120px;margin:auto;--rp-accent:var(--global-theme-color,#2563eb)}
.research-intro{color:var(--global-text-color-light);font-size:1.06rem;margin:0 0 1.6rem}
.research-list{display:grid;grid-template-columns:1fr;gap:1.3rem}
.research-card{position:relative;border:1px solid var(--global-divider-color,#ddd);background:var(--global-card-bg-color,transparent);border-radius:16px;padding:1.6rem 1.8rem;box-shadow:0 5px 22px rgba(0,0,0,.045);overflow:hidden}
.research-card:before{content:"";position:absolute;top:0;left:0;height:5px;width:100%;background:var(--rp-accent)}
.research-card-top{display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:.5rem;margin-bottom:.8rem}
.research-number{color:var(--rp-accent);font-size:.78rem;font-weight:800;letter-spacing:.1em}
.research-date{font-size:.89rem;color:var(--global-text-color-light);font-weight:650}
.research-card h2{font-size:1.42rem;font-weight:750;line-height:1.35;margin:0 0 1.1rem}
.research-meta{display:grid;grid-template-columns:minmax(180px,1fr) minmax(0,2fr);gap:.8rem;padding:.95rem 1rem;border-radius:10px;background:rgba(100,120,180,.065);margin-bottom:1.1rem}
.research-meta>div{display:flex;flex-direction:column;gap:.2rem}
.research-label{font-size:.76rem;letter-spacing:.02em;color:var(--rp-accent);font-weight:750;text-transform:uppercase}
.research-card h3{font-weight:750;font-size:1.03rem;color:var(--rp-accent);margin:1.05rem 0 .45rem}
.research-card p{margin:.25rem 0 .65rem}
.research-card ul{padding-left:1.4rem;margin:.5rem 0 .3rem}
.research-card li{margin:.42rem 0;line-height:1.65}
.research-details{margin-top:1.2rem;border-top:1px solid var(--global-divider-color,#ddd);padding-top:.8rem}
.research-details summary{cursor:pointer;color:var(--rp-accent);font-weight:750;list-style-position:outside;padding:.25rem 0}
.research-details summary:focus-visible{outline:2px solid var(--rp-accent);outline-offset:3px}
.research-count{display:inline-block;padding:.1rem .45rem;border-radius:20px;background:rgba(100,120,180,.1);font-size:.76rem;margin-left:.3rem}
@media(max-width:650px){.research-card{padding:1.2rem}.research-meta{grid-template-columns:1fr}.research-card h2{font-size:1.2rem}}
.research-card{padding:0!important}.research-project-toggle{display:block;cursor:pointer;position:relative;padding:1.05rem 3.6rem 1.05rem 1.4rem;list-style:none}.research-project-toggle::-webkit-details-marker{display:none}.research-project-toggle::marker{content:""}.research-project-title{font-size:1.13rem;line-height:1.45;font-weight:750;display:block}.research-project-toggle .research-card-top{margin-bottom:.3rem}.research-chevron{position:absolute;right:1.4rem;top:50%;transform:translateY(-50%);color:var(--rp-accent);transition:transform .2s}.research-card[open] .research-chevron{transform:translateY(-50%) rotate(180deg)}.research-card-body{padding:0 1.5rem 1.5rem}.research-card[open]{border-color:var(--rp-accent)}.research-project-toggle:hover,.research-project-toggle:focus-visible{background:rgba(100,120,180,.06)}.research-project-toggle:focus-visible{outline:2px solid var(--rp-accent);outline-offset:-3px}.research-list{gap:.75rem}.research-card .research-details{margin-top:1rem}
/* Keep page titles in navigation, not repeated above the content. */
.post-header .post-title,.post-header h1,.page-header .page-title{display:none!important}

/* Hide only the automatic duplicate page heading, preserving all content headings. */
.post-header,.page-header{display:none!important}
.research-project-toggle{display:flex!important;align-items:center;justify-content:space-between;gap:1rem;flex-wrap:nowrap;padding:1rem 3.5rem 1rem 1.35rem;min-height:68px}
.research-project-toggle .research-project-title{flex:1 1 auto;min-width:0;line-height:1.35;margin:0;font-size:1.08rem}
.research-project-toggle .research-date{flex:0 0 auto;white-space:nowrap;text-align:right;font-size:.84rem}
@media(max-width:650px){.research-project-toggle{gap:.55rem;padding:.85rem 2.25rem .85rem .8rem}.research-project-toggle .research-project-title{font-size:.88rem}.research-project-toggle .research-date{font-size:.7rem}.research-chevron{right:.7rem}}
</style>

<div class="research-projects">
  <p class="research-intro">Selected research projects across biomedical AI, climate risk forecasting, deep learning optimization, computer vision, and intelligent systems.</p>
  <div class="research-list">
  <details class="research-card" id="research-project-1">
    <summary class="research-project-toggle"><span class="research-project-title">AI-based Histopathology</span><span class="research-date"><i class="fa-regular fa-calendar" aria-hidden="true"></i> 10/2024 – 10/2026</span><i class="fa-solid fa-chevron-down research-chevron" aria-hidden="true"></i></summary><div class="research-card-body">
    <div class="research-meta"><div><span class="research-label"><i class="fa-solid fa-user-gear" aria-hidden="true"></i> Role</span><strong>Post-doctoral Scholar</strong></div><div><span class="research-label"><i class="fa-solid fa-building-columns" aria-hidden="true"></i> Funder</span><span>National Institutes of Health (NIH), USA.</span></div></div>
    <h3>Objectives</h3><p>Develop end-to-end WSI and multimodal analysis workflows for histopathology.</p>
    <div class="research-details"><h3><i class="fa-solid fa-list-check" aria-hidden="true"></i> Responsibilities <span class="research-count">9</span></h3><ul><li>Building end-to-end pipelines for whole-slide image (WSI) and tile-level tissue classification and segmentation.</li><li>Developing a RAG-based pipeline integrating PathologyBERT, ChromaDB, Grounding DINO, and SAM2 for text-guided SRC localization and segmentation-based pseudo-annotation of 512 × 512 histopathology tiles.</li><li>Integrating RAG, PathologyBERT, ChromaDB, and CONCH for morphology-guided retrieval and diverse sample selection across nine colorectal tissue classes using 256 × 256 tiles, with QuPath-based verification.</li><li>Implementing autoencoder-based, multi-task preprocessing for pathology images covering artifact filtering, tile extraction, and quality control, to deliver clean, consistent inputs at scale.</li><li>Managing multiple GPU resources to run large-scale image analytics.</li><li>Training and deploying multimodal pathology foundation models (image + text) for analysis and report generation.</li><li>Annotating tumor regions in WSIs with QuPath to produce high-quality ground truth for model development.</li><li>Curating a large tile-level tissue dataset to support benchmarking and reproducible research.</li><li>Developing a patch- and cell-level segmentation model to detect signet ring cells.</li></ul></div>
  </div></details>
<details class="research-card" id="research-project-2">
    <summary class="research-project-toggle"><span class="research-project-title">AI-Driven Climate Risk Assessment at the Hanford Site</span><span class="research-date"><i class="fa-regular fa-calendar" aria-hidden="true"></i> 08/2023 – 09/2024</span><i class="fa-solid fa-chevron-down research-chevron" aria-hidden="true"></i></summary><div class="research-card-body">
    <div class="research-meta"><div><span class="research-label"><i class="fa-solid fa-user-gear" aria-hidden="true"></i> Role</span><strong>Project Associate</strong></div><div><span class="research-label"><i class="fa-solid fa-building-columns" aria-hidden="true"></i> Funder</span><span>U.S. Department of Energy (DOE), Office of Environmental Management, Minority Serving Institution Partnership Program (MSIPP), in collaboration with University of Houston-Victoria.</span></div></div>
    <h3>Objectives</h3><p>Apply AI-based climate forecasting to assess environmental risk factors at the Hanford Site.</p>
    <div class="research-details"><h3><i class="fa-solid fa-list-check" aria-hidden="true"></i> Responsibilities <span class="research-count">4</span></h3><ul><li>Developing multivariate sequence models (LSTM, GRU, attention) to forecast groundwater contamination.</li><li>Generating realistic sequential synthetic data using GANs and diffusion models to augment limited observations.</li><li>Imputing missing values and subsequences in time-series data to improve model fidelity.</li><li>Implementing Transformer architectures for long-horizon forecasting of environmental time-series datasets.</li></ul></div>
  </div></details>
<details class="research-card" id="research-project-3">
    <summary class="research-project-toggle"><span class="research-project-title">Optimizer Enhancements for Deep Neural Networks</span><span class="research-date"><i class="fa-regular fa-calendar" aria-hidden="true"></i> 05/2022 – 05/2023</span><i class="fa-solid fa-chevron-down research-chevron" aria-hidden="true"></i></summary><div class="research-card-body">
    <div class="research-meta"><div><span class="research-label"><i class="fa-solid fa-user-gear" aria-hidden="true"></i> Role</span><strong>Project Lead</strong></div><div><span class="research-label"><i class="fa-solid fa-building-columns" aria-hidden="true"></i> Funder</span><span>School of Computer Science and Engineering, Kyungpook National University, South Korea.</span></div></div>
    <h3>Objectives</h3><ul><li>Improving model reliability by accelerating convergence of gradient-based optimizers (e.g., SGD, Adam).</li><li>Enhancing nonlinear representational capacity using modified activation functions to capture complex relationships.</li></ul>
    <div class="research-details"><h3><i class="fa-solid fa-list-check" aria-hidden="true"></i> Responsibilities <span class="research-count">5</span></h3><ul><li>Designing and implementing deep learning models to evaluate the proposed methods.</li><li>Integrating the proposed methods into TensorFlow by overriding core modules.</li><li>Developing mathematical proofs and theoretical analyses of the proposed methods.</li><li>Provisioning a distributed compute cluster and a shareable GPU server to support experiments.</li><li>Running experiments and conducting empirical analyses and ablation studies.</li></ul></div>
  </div></details>
<details class="research-card" id="research-project-4">
    <summary class="research-project-toggle"><span class="research-project-title">Automated Fabric Defect Detection and Visualization</span><span class="research-date"><i class="fa-regular fa-calendar" aria-hidden="true"></i> 09/2022 – 05/2023</span><i class="fa-solid fa-chevron-down research-chevron" aria-hidden="true"></i></summary><div class="research-card-body">
    <div class="research-meta"><div><span class="research-label"><i class="fa-solid fa-user-gear" aria-hidden="true"></i> Role</span><strong>Project Associate</strong></div><div><span class="research-label"><i class="fa-solid fa-building-columns" aria-hidden="true"></i> Funder</span><span>National Research Foundation (NRF), South Korea.</span></div></div>
    <h3>Objectives</h3><p>Detect and localize abnormalities in fabric products.</p>
    <div class="research-details"><h3><i class="fa-solid fa-list-check" aria-hidden="true"></i> Responsibilities <span class="research-count">5</span></h3><ul><li>Applied targeted data augmentation to expand the training set and improve model generalization.</li><li>Built a preprocessing pipeline (denoising, contrast enhancement) to improve image quality.</li><li>Developed and evaluated autoencoder-based methods for anomaly localization.</li><li>Benchmarked models on anomaly-detection datasets and performed error analysis and ablations.</li><li>Documented experiments, configurations, and results to ensure reproducibility.</li></ul></div>
  </div></details>
<details class="research-card" id="research-project-5">
    <summary class="research-project-toggle"><span class="research-project-title">Real-time Fault Detection in Fused Deposition Modelling</span><span class="research-date"><i class="fa-regular fa-calendar" aria-hidden="true"></i> 07/2022 – 10/2022</span><i class="fa-solid fa-chevron-down research-chevron" aria-hidden="true"></i></summary><div class="research-card-body">
    <div class="research-meta"><div><span class="research-label"><i class="fa-solid fa-user-gear" aria-hidden="true"></i> Role</span><strong>Project Associate</strong></div><div><span class="research-label"><i class="fa-solid fa-building-columns" aria-hidden="true"></i> Funder</span><span>Department of Mechanical Engineering, National Institute of Technology Calicut, India, in collaboration with the School of Computer Science and Engineering, Kyungpook National University, South Korea.</span></div></div>
    <h3>Objectives</h3><p>Real-time error detection in fused deposition modelling using CNNs.</p>
    <div class="research-details"><h3><i class="fa-solid fa-list-check" aria-hidden="true"></i> Responsibilities <span class="research-count">4</span></h3><ul><li>Collecting sample images across defect categories—staircase, overfill, and void—during fused deposition modelling (FDM).</li><li>Generating additional images via targeted data augmentation to mitigate overfitting.</li><li>Designing a convolutional neural network (CNN) to train and classify defect types.</li><li>Benchmarking the proposed approach against standardized classification algorithms.</li></ul></div>
  </div></details>
<details class="research-card" id="research-project-6">
    <summary class="research-project-toggle"><span class="research-project-title">Gesture Recognition System for Sign Language and Music Generation</span><span class="research-date"><i class="fa-regular fa-calendar" aria-hidden="true"></i> 02/2022 – 05/2023</span><i class="fa-solid fa-chevron-down research-chevron" aria-hidden="true"></i></summary><div class="research-card-body">
    <div class="research-meta"><div><span class="research-label"><i class="fa-solid fa-user-gear" aria-hidden="true"></i> Role</span><strong>Project Coordinator</strong></div><div><span class="research-label"><i class="fa-solid fa-building-columns" aria-hidden="true"></i> Funder</span><span>School of Computer Science and Engineering, Kyungpook National University, South Korea.</span></div></div>
    <h3>Objectives</h3><ul><li>Real-time music generation driven by hand-gesture recognition.</li><li>Sign-language recognition from hand gestures.</li></ul>
    <div class="research-details"><h3><i class="fa-solid fa-list-check" aria-hidden="true"></i> Responsibilities <span class="research-count">5</span></h3><ul><li>Modified a GRU model to enhance gesture recognition accuracy and performance.</li><li>Developed a validation framework to ensure model effectiveness across various gesture types for maintaining project quality standards.</li><li>Coordinated the technical integration of deep learning models with application interfaces, streamlining real-time translation of recognized gestures into output.</li><li>Managed technical documentation and project guidelines, supporting project scalability and knowledge transfer.</li><li>Facilitated collaboration between technical and user experience teams to optimize interface design for gesture-based applications.</li></ul></div>
  </div></details>
<details class="research-card" id="research-project-7">
    <summary class="research-project-toggle"><span class="research-project-title">Korean Handwritten Text Recognition</span><span class="research-date"><i class="fa-regular fa-calendar" aria-hidden="true"></i> 12/2021 – 02/2022</span><i class="fa-solid fa-chevron-down research-chevron" aria-hidden="true"></i></summary><div class="research-card-body">
    <div class="research-meta"><div><span class="research-label"><i class="fa-solid fa-user-gear" aria-hidden="true"></i> Role</span><strong>Project Technical Support Specialist</strong></div><div><span class="research-label"><i class="fa-solid fa-building-columns" aria-hidden="true"></i> Funder</span><span>Medium Business Technology Information Promotion Agency, South Korea.</span></div></div>
    <h3>Objectives</h3><p>Generate Korean text from old-fashioned Korean handwriting.</p>
    <div class="research-details"><h3><i class="fa-solid fa-list-check" aria-hidden="true"></i> Responsibilities <span class="research-count">4</span></h3><ul><li>Annotated bounding boxes for handwritten text datasets.</li><li>Engineered a preprocessing pipeline using histogram of oriented gradients (HOG) and contrast normalization to extract robust stroke features.</li><li>Contributed to a Bi-LSTM-based OCR model for handwriting transcription.</li><li>Evaluated performance with character error rate (CER) and conducted error analyses to guide model improvements.</li></ul></div>
  </div></details>
<details class="research-card" id="research-project-8">
    <summary class="research-project-toggle"><span class="research-project-title">Object Detection in Manufacturing and Smart City</span><span class="research-date"><i class="fa-regular fa-calendar" aria-hidden="true"></i> 03/2021 – 02/2022</span><i class="fa-solid fa-chevron-down research-chevron" aria-hidden="true"></i></summary><div class="research-card-body">
    <div class="research-meta"><div><span class="research-label"><i class="fa-solid fa-user-gear" aria-hidden="true"></i> Role</span><strong>Project Associate</strong></div><div><span class="research-label"><i class="fa-solid fa-building-columns" aria-hidden="true"></i> Funder</span><span>Medium Business Technology Information Promotion Agency, South Korea.</span></div></div>
    <h3>Objectives</h3><ul><li>Automated detection of illegal parking in accessible (disabled) spaces.</li><li>Automated detection of improperly placed objects (e.g., stickers, badges).</li></ul>
    <div class="research-details"><h3><i class="fa-solid fa-list-check" aria-hidden="true"></i> Responsibilities <span class="research-count">4</span></h3><ul><li>Collected on-site imagery of accessible parking spaces to build a diverse training set.</li><li>Preprocessed and annotated images to label illegal-parking cases and object placement issues (e.g., stickers, badges).</li><li>Identified and benchmarked suitable deep learning architectures for automated detection, selecting the best-performing model.</li><li>Conducted iterative testing, error analysis, and model tuning to improve detection accuracy.</li></ul></div>
  </div></details>
</div>
</div>
