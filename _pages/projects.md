---
layout: archive
title: "Selected Projects"
permalink: /projects/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

---

---

<!-- 项目块开始 -->
<div style="display: flex; flex-wrap: wrap; gap: 20px; margin-bottom: 40px; align-items: flex-start; border-bottom: 1px solid #eee; padding-bottom: 20px;">

  <!-- 左侧：视频区域 -->
  <div style="flex: 0 0 320px; max-width: 100%; position: relative;">
    <!-- 标签 Badge -->
    <div style="position: absolute; top: 10px; left: 10px; background-color: #003366; color: white; padding: 4px 8px; font-size: 12px; font-weight: bold; z-index: 5; border-radius: 3px; opacity: 0.9;">
      Under Review
    </div>
    
    <!-- 视频播放器 -->
    <video width="100%" autoplay loop muted playsinline controls style="border-radius: 6px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); display: block;">
      <!-- 注意：这里加了斜杠 /files/... -->
      <source src="/files/trajectory_optimization.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>

  <!-- 右侧：文字区域 -->
  <div style="flex: 1; min-width: 300px;">
    <h3 style="margin-top: 0; margin-bottom: 10px; font-size: 1.2rem; line-height: 1.4;">
     **G**pu-accelerated **U**nderwater **I**ntelligent **D**ifferential **E**volution for collision-free 3D path planning of autonomous gliders in dynamic ocean currents
    </h3>
    
    <div style="color: #555; font-size: 0.95rem; margin-bottom: 10px;">
      <strong>Your Name*</strong>, Collaborator Name*, Collaborator Name, Advisor Name
    </div>

    <div style="margin-bottom: 12px;">
      <a href="https://your-link" style="margin-right: 10px; text-decoration: none; color: #0066cc; font-weight: bold;">[Website&Video]</a>
      <a href="https://your-link" style="margin-right: 10px; text-decoration: none; color: #0066cc; font-weight: bold;">[PDF]</a>
      <a href="https://your-link" style="text-decoration: none; color: #0066cc; font-weight: bold;">[BibTeX]</a>
    </div>

    <p style="font-size: 0.9rem; line-height: 1.6; color: #333; margin: 0;">
      <strong>TLDR:</strong> GUIDE is a novel path planning framework that integrates <strong>ocean current domain knowledge</strong> into evolutionary search (LSHADE-AHF) and utilizes <strong>GPU parallelism</strong> to solve high-dimensional 3D trajectory problems in seconds. It ensures strict collision avoidance with high-resolution GEBCO terrain data.
    </p>
  </div>

</div>
<!-- 项目块结束 -->

---

Education
======
* Ph.D in Version Control Theory, GitHub University, 2018 (expected)
* M.S. in Jekyll, GitHub University, 2014
* B.S. in GitHub, GitHub University, 2012

Work experience
======
* Spring 2024: Academic Pages Collaborator
  * Github University
  * Duties includes: Updates and improvements to template
  * Supervisor: The Users

* Fall 2015: Research Assistant
  * Github University
  * Duties included: Merging pull requests
  * Supervisor: Professor Hub

* Summer 2015: Research Assistant
  * Github University
  * Duties included: Tagging issues
  * Supervisor: Professor Git
  
Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* Currently signed in to 43 different slack teams
