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
      GUIDE: <strong>G</strong>PU-accelerated <strong>U</strong>nderwater <strong>I</strong>ntelligent <strong>D</strong>ifferential <strong>E</strong>volution for Collision-Free 3D Path Planning of Autonomous Gliders in Dynamic Ocean Currents
    </h3>
    
    <!-- 作者 -->
    <div style="opacity: 0.85; font-size: 1rem; margin-bottom: 15px;">
      <strong>Zezhong Li*</strong>, Zhong-ke Gao
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
        <strong>GUIDE</strong> is a state-of-the-art path planning framework designed for <strong>Autonomous Underwater Gliders (AUGs)</strong> operating in complex, time-varying ocean environments. Unlike traditional planners, GUIDE directly integrates <strong>domain knowledge (Ocean Currents)</strong> into the evolutionary search process. By leveraging massive <strong>GPU parallelism</strong> and a custom "Whole-Trajectory Kernel," it solves high-dimensional 3D trajectory optimization problems in seconds, reducing runtime by orders of magnitude (e.g., from ~1800s to <150s).
      </p>
      <p style="margin-bottom: 0;">
        The framework introduces a novel <strong>Adaptive Hybrid Flow</strong> mutation strategy, intelligently switching between "Current-Guided Search" and "Stochastic Exploration" to prevent stagnation in vortexes. It ensures strict safety using <strong>SDF-based GPU Sphere Tracing</strong> against high-resolution <strong>GEBCO</strong> seabed data, while fully accounting for <strong>4D time-varying dynamics</strong> to optimize both energy and time efficiency.
      </p>
    </div>

    <!-- 特性列表 (用来填充高度，增加可读性) -->
    <div style="background: rgba(128,128,128, 0.05); padding: 15px; border-radius: 8px; border: 1px solid rgba(128,128,128, 0.1);">
      <h4 style="margin: 0 0 10px 0; font-size: 1rem; font-weight: bold;">Key Highlights:</h4>
      <ul style="margin: 0; padding-left: 20px; font-size: 0.9rem; line-height: 1.5; opacity: 0.85;">
        <li style="margin-bottom: 8px;">🚀 <strong>Extreme GPU Performance:</strong> Built on CUDA to eliminate CPU-GPU bottlenecks.</li>
        <li style="margin-bottom: 8px;">🌊 <strong>Physics-Informed Evolution:</strong> Utilizes flow vectors to guide evolutionary search.</li>
        <li style="margin-bottom: 8px;">🛡️ <strong>Strict 3D Avoidance:</strong> Collision-free paths via Signed Distance Fields (SDF).</li>
        <li>⏳ <strong>Time-Varying Dynamics:</strong> Full support for 4D CMEMS ocean data.</li>
      </ul>
    </div>

  </div>

</div>
<!-- 项目结束 -->

<hr style="border: 0; border-top: 1px solid rgba(128,128,128, 0.2); margin: 40px 0;">

</div>
<!-- 项目结束 -->

<hr style="border: 0; border-top: 1px solid rgba(128,128,128, 0.2); margin: 40px 0;">
