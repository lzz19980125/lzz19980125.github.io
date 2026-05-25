---
layout: archive
title: "Selected Projects"
permalink: /projects/
author_profile: true
redirect_from:
  - /resume
---

<hr style="border: 0; border-top: 1px solid rgba(128,128,128, 0.2); margin: 20px 0 40px 0;">

<!-- 项目卡片容器 -->
<div style="display: flex; flex-wrap: wrap; gap: 30px; margin-bottom: 50px; align-items: flex-start;">

  <!-- 左侧：视频区域容器 (垂直排列) -->
  <div style="flex: 1 1 450px; min-width: 300px; display: flex; flex-direction: column; gap: 15px;">
    
    <!-- 视频 1：3D Vision -->
    <div style="position: relative;">
      <!-- 标签 Badge -->
      <div style="position: absolute; bottom: 12px; left: 12px; background-color: #0056b3; color: white; padding: 4px 10px; font-size: 0.8rem; font-weight: bold; z-index: 5; border-radius: 4px; box-shadow: 0 2px 4px rgba(0,0,0,0.3); letter-spacing: 0.5px;">
        3D Vision
      </div>
      <!-- 视频播放器 -->
      <video width="100%" autoplay loop muted playsinline controls style="border-radius: 8px; box-shadow: 0 5px 15px rgba(0,0,0,0.2); display: block; border: 1px solid rgba(128,128,128, 0.2);">
        <source src="/files/trajectory_optimization.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>

    <!-- 视频 2：2D Flow (新增) -->
    <div style="position: relative;">
      <!-- 标签 Badge -->
      <div style="position: absolute; bottom: 12px; left: 12px; background-color: #0056b3; color: white; padding: 4px 10px; font-size: 0.8rem; font-weight: bold; z-index: 5; border-radius: 4px; box-shadow: 0 2px 4px rgba(0,0,0,0.3); letter-spacing: 0.5px;">
        2D Vision
      </div>
      <!-- 视频播放器 -->
      <video width="100%" autoplay loop muted playsinline controls style="border-radius: 8px; box-shadow: 0 5px 15px rgba(0,0,0,0.2); display: block; border: 1px solid rgba(128,128,128, 0.2);">
        <source src="/files/trajectory_optimization_2D.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>

  </div>

<!-- 右侧：文字区域 -->
  <div style="flex: 1 1 400px; min-width: 300px; padding-left: 10px;">
    
    <!-- 标题 -->
    <h3 style="margin-top: 0; margin-bottom: 15px; font-size: 1.4rem; line-height: 1.3; font-weight: 800;">
      MadDE-NDA: Collision-Free Time-Optimal Planning of Underwater Gliders in Time-Varying Currents via Adaptive <strong>N</strong>iching <strong>D</strong>ual-<strong>A</strong>rchive Differential Evolution
    </h3>
    
    <!-- 作者 -->
    <div style="opacity: 0.85; font-size: 1rem; margin-bottom: 15px;">
      <strong>Zezhong Li</strong>, Rongshun Juan, Yang Li, Shoufu Liu, Tianshu Wang, Shuaikun Shi, Leihao Du, Wanjun Feng, Zhongke Gao*
    </div>

    <!-- 链接按钮 -->
    <div style="margin-bottom: 25px;">
      <a href="https://rapid-route.github.io/" style="display: inline-block; background: rgba(0, 123, 255, 0.1); color: #007bff; padding: 6px 12px; border-radius: 4px; text-decoration: none; font-weight: bold; border: 1px solid rgba(0, 123, 255, 0.2); transition: all 0.3s; font-size: 0.9rem;">
        [Website & Video]
      </a>
    </div>

    <!-- 详细摘要 (扩充版) -->
    <div style="font-size: 0.95rem; line-height: 1.6; opacity: 0.9; text-align: justify; margin-bottom: 20px;">
      <p style="margin-bottom: 15px;">
        We propose a highly efficient <strong>GPU-accelerated 4D path planning framework</strong> for Autonomous Underwater Gliders (AUGs) operating in complex, time-varying ocean currents. To overcome the curse of dimensionality inherent in long-range missions, we introduce a fixed-dimensional <strong>B-spline trajectory encoding</strong>. Dynamic feasibility is strictly verified through <strong>RK4 integration</strong>, while continuous-domain collision safety over complex seabed topography is guaranteed using an <strong>ESDF-based Sphere Tracing</strong> strategy, eliminating the tunneling effect seen in traditional discrete sampling.
      </p>
      <p style="margin-bottom: 0;">
        To tackle the highly multimodal search landscape induced by ocean currents and terrain, we develop a novel optimizer named <strong>MadDE-NDA</strong> (Niching Dual-Archive). It features dual cooperative archives to balance quality retention and diversity preservation, coupled with a stagnation-triggered niching mechanism. Accelerated by massive GPU parallelism for population-level evaluation, the framework demonstrates superior safety, efficiency, and robustness in realistic simulations utilizing high-resolution <strong>GEBCO</strong> bathymetry and <strong>CMEMS</strong> spatiotemporal ocean currents.
      </p>
    </div>

</div>
<!-- 项目结束 -->

<hr style="border: 0; border-top: 1px solid rgba(128,128,128, 0.2); margin: 40px 0;">

</div>
<!-- 项目结束 -->

<hr style="border: 0; border-top: 1px solid rgba(128,128,128, 0.2); margin: 40px 0;">
