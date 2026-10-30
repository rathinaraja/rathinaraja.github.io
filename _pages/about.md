---
layout: about
title: About
permalink: /
nav: true
nav_order: 1
subtitle: '<span style="color:#6A1B9A;">Researcher, Stanford University, Palo Alto, USA</span>'

profile:
  align: right
  image: prof_pic.jpeg
  image_circular: false # crops the image to make it circular
  more_info: > 
    <p style="font-size: 0.75em; font-style: italic;">
      Look at everything as an infant does; absorbing everything, not judging anything, not labelling anyone!!!
    </p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 3 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

I work at the intersection of machine learning, computer vision, multimodal learning, and healthcare, with a focus on biomedical and clinical AI. My research interests include large language models (LLMs), vision-language models (VLMs), foundation models, and trustworthy AI for clinical decision support.

My work focuses on building end-to-end AI pipelines, from data preparation and system design to model development, evaluation, deployment, and maintenance. I develop scalable deep learning and multimodal systems for whole-slide image preprocessing, multiple instance learning, classification, segmentation, survival prediction, and image-text modeling, and build Streamlit applications to support clinical and research use. A major part of my work involves improving data quality, model generalizability, and reliability for tumor diagnosis, subtyping, biomarker prediction, segmentation, and survival analysis. I also have experience with GPU infrastructure, large-scale datasets, and distributed computing.

My research philosophy is simple: build reliable data, develop generalizable models, and deliver interpretable, reproducible, and practically useful AI systems.

<style>
/* Profile portrait: comfortable desktop sizing and a phone-friendly stacked layout. */
.profile {
  width: clamp(235px, 29%, 320px) !important;
  max-width: 100%;
  margin-left: 1.6rem;
  margin-bottom: 1.2rem;
}
.profile img,
.profile .img-fluid {
  display: block;
  width: 100%;
  height: auto;
  object-fit: contain;
  border-radius: 12px;
}
.profile .more-info,
.profile .more-info p {
  overflow-wrap: break-word;
  word-break: normal;
  line-height: 1.55;
}
.profile .more-info p {
  font-size: .86rem !important;
  text-align: center;
  margin: .8rem 0 0;
  padding: 0 .4rem;
}
@media (max-width: 767px) {
  .profile,
  .profile.float-right,
  .profile.float-left {
    float: none !important;
    width: min(100%, 340px) !important;
    max-width: 100% !important;
    margin: 0 auto 1.7rem !important;
    padding: 0 !important;
  }
  .profile img,
  .profile .img-fluid {
    width: 100% !important;
    max-width: 340px;
    height: auto !important;
    margin: 0 auto;
  }
  .profile .more-info,
  .profile .more-info p {
    width: 100%;
    max-width: 340px;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>
