---
layout: archive
title: "Selected Projects"
permalink: /projects/
author_profile: true
redirect_from:
  - /resume
---

<!-- 项目卡片容器 -->
<div style="display: flex; flex-wrap: wrap; gap: 30px; margin-bottom: 50px; align-items: center;">

  <!-- 左侧：视频区域 (放大版) -->
  <div style="flex: 1 1 450px; position: relative; min-width: 300px;">
    <!-- 标签 Badge (已修改位置到左下角) -->
    <div style="position: absolute; bottom: 12px; left: 12px; background-color: #0056b3; color: white; padding: 4px 10px; font-size: 0.8rem; font-weight: bold; z-index: 5; border-radius: 4px; box-shadow: 0 2px 4px rgba(0,0,0,0.3); letter-spacing: 0.5px;">
      3D Vision
    </div>
    
    <!-- 视频播放器 -->
    <video width="100%" autoplay loop muted playsinline controls style="border-radius: 8px; box-shadow: 0 5px 15px rgba(0,0,0,0.2); display: block; border: 1px solid rgba(128,128,128, 0.2);">
      <source src="/files/trajectory_optimization.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>

  <!-- 右侧：文字区域 -->
  <div style="flex: 1 1 400px; min-width: 300px;">
    
    <!-- 标题 -->
    <h3 style="margin-top: 0; margin-bottom: 15px; font-size: 1.4rem; line-height: 1.3; font-weight: 800;">
      GUIDE: <strong>G</strong>PU-accelerated <strong>U</strong>nderwater <strong>I</strong>ntelligent <strong>D</strong>ifferential <strong>E</strong>volution for Collision-Free 3D Path Planning of Autonomous Gliders in Dynamic Ocean Currents
    </h3>
    
    <!-- 作者 -->
    <div style="opacity: 0.85; font-size: 1rem; margin-bottom: 15px;">
      <strong>Zezhong Li*</strong>, Zhong-ke Gao
    </div>

    <!-- 链接按钮 -->
    <div style="margin-bottom: 20px;">
      <a href="https://rapid-route.github.io/" style="display: inline-block; background: rgba(0, 123, 255, 0.1); color: #007bff; padding: 5px 10px; border-radius: 4px; text-decoration: none; font-weight: bold; border: 1px solid rgba(0, 123, 255, 0.2); transition: all 0.3s;">
        [Website & Video]
      </a>
    </div>

    <!-- 摘要 -->
    <p style="font-size: 0.95rem; line-height: 1.6; opacity: 0.9; margin: 0; text-align: justify;">
      <strong>TLDR:</strong> <strong>GUIDE</strong> is a state-of-the-art path planning framework designed for <strong>Autonomous Underwater Gliders (AUGs)</strong> operating in complex, time-varying ocean environments. Unlike traditional planners, GUIDE integrates <strong>domain knowledge (Ocean Currents)</strong> directly into the evolutionary search process and leverages massive <strong>GPU parallelism</strong> to solve high-dimensional 3D trajectory optimization problems in seconds.
    </p>
  </div>

</div>
<!-- 项目结束 -->

<hr style="border: 0; border-top: 1px solid rgba(128,128,128, 0.2); margin: 40px 0;">
