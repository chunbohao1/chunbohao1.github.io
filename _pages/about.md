---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

I am a first-year Master's student at the Northwestern Polytechnical University, supervised by Prof. [Lei Xie](http://lxie.npu-aslp.org/).

My research interest includes speech synthesis and song generation.

## 🔍 Research Area
- Speech Processing: Text-to-Speech
- Music Generation: Song Generation, Singing Voice Synthesis, Music Information Retrieval 

# 📝 Publications

- <span style="display:inline-block; background-color:#6c757d; color:#fff; padding:0px 7px; margin-right:5px; font-size:13px;">Under Review</span> YingMusic-Singer: Controllable Singing Voice Synthesis with Flexible Lyric Manipulation and Annotation-free Melody Guidance **C Hao**, J Zheng, G Ma, Y Jiang, H Chen, W Tian, G Chen, Z Chen, L Xie. [[PDF]](https://arxiv.org/pdf/2603.24589) [[DemoPage]](https://aslp-lab.github.io/YingMusic-Singer-Demo) [[GitHub]](https://github.com/ASLP-lab/YingMusic-Singer)

- <span style="display:inline-block; background-color:#f5bd42; color:#fff; padding:0px 7px; margin-right:5px; font-size:13px;">CCF-B ICME 2026</span> SongFormer: Scaling Music Structure Analysis with Heterogeneous Supervision **C Hao**, **R Yuan**, J Yao, Q Deng, X Bai, W Xue, L Xie. [[PDF]](https://arxiv.org/pdf/2510.02797) [[Github]](https://github.com/ASLP-lab/SongFormer)
