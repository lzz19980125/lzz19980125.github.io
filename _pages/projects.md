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
        <source src="/files/case_1_3D.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
    
    <!-- 视频 2：3D Flow (新增) -->
    <div style="position: relative;">
      <!-- 标签 Badge -->
      <div style="position: absolute; bottom: 12px; left: 12px; background-color: #0056b3; color: white; padding: 4px 10px; font-size: 0.8rem; font-weight: bold; z-index: 5; border-radius: 4px; box-shadow: 0 2px 4px rgba(0,0,0,0.3); letter-spacing: 0.5px;">
        3D Vision
      </div>
      <!-- 视频播放器 -->
      <video width="100%" autoplay loop muted playsinline controls style="border-radius: 8px; box-shadow: 0 5px 15px rgba(0,0,0,0.2); display: block; border: 1px solid rgba(128,128,128, 0.2);">
        <source src="/files/case_2_3D.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
    
    <!-- 视频 3：3D Flow (新增) -->
    <div style="position: relative;">
      <!-- 标签 Badge -->
      <div style="position: absolute; bottom: 12px; left: 12px; background-color: #0056b3; color: white; padding: 4px 10px; font-size: 0.8rem; font-weight: bold; z-index: 5; border-radius: 4px; box-shadow: 0 2px 4px rgba(0,0,0,0.3); letter-spacing: 0.5px;">
        3D Vision
      </div>
      <!-- 视频播放器 -->
      <video width="100%" autoplay loop muted playsinline controls style="border-radius: 8px; box-shadow: 0 5px 15px rgba(0,0,0,0.2); display: block; border: 1px solid rgba(128,128,128, 0.2);">
        <source src="/files/case_5_3D.mp4" type="video/mp4">
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

<!-- 按钮容器：使用 display: flex 让内部元素水平排列，gap 控制间距 -->

<div style="margin-bottom: 25px; display: flex; gap: 15px;">


  <a href="https://rapid-route.github.io/" style="display: inline-block; background: rgba(0, 123, 255, 0.1); color: #007bff; padding: 6px 12px; border-radius: 4px; text-decoration: none; font-weight: bold; border: 1px solid rgba(0, 123, 255, 0.2); transition: all 0.3s; font-size: 0.9rem;">
    [Website & Video]
  </a>

  <a href="https://rapid-route.github.io/index_cn.html" style="display: inline-block; background: rgba(0, 123, 255, 0.1); color: #007bff; padding: 6px 12px; border-radius: 4px; text-decoration: none; font-weight: bold; border: 1px solid rgba(0, 123, 255, 0.2); transition: all 0.3s; font-size: 0.9rem;">
    [中文网站 & 视频]
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


<!-- CargoForge3D Project -->

<div style="display: flex; flex-wrap: wrap; gap: 30px; margin-bottom: 50px; align-items: flex-start;">


  <!-- Left: project figures -->

  <div style="flex: 1 1 450px; min-width: 300px; display: flex; flex-direction: column; gap: 15px;">
    <div style="position: relative;">
      <div style="position: absolute; bottom: 12px; left: 12px; background-color: #0056b3; color: white; padding: 4px 10px; font-size: 0.8rem; font-weight: bold; z-index: 5; border-radius: 4px; box-shadow: 0 2px 4px rgba(0,0,0,0.3); letter-spacing: 0.5px;">
        Algorithm Overview
      </div>
      <img src="https://cargo-forge3d.github.io/resources/figures/cargo-forge3d-algorithm-overview.png" alt="CargoForge3D algorithm overview" style="width: 100%; border-radius: 8px; box-shadow: 0 5px 15px rgba(0,0,0,0.2); display: block; border: 1px solid rgba(128,128,128, 0.2);">
    </div>


    <div style="position: relative;">
      <div style="position: absolute; bottom: 12px; left: 12px; background-color: #0056b3; color: white; padding: 4px 10px; font-size: 0.8rem; font-weight: bold; z-index: 5; border-radius: 4px; box-shadow: 0 2px 4px rgba(0,0,0,0.3); letter-spacing: 0.5px;">
        Serving Architecture
      </div>
      <img src="https://cargo-forge3d.github.io/resources/figures/cargo-forge3d-system-architecture.png" alt="CargoForge3D system architecture" style="width: 100%; border-radius: 8px; box-shadow: 0 5px 15px rgba(0,0,0,0.2); display: block; border: 1px solid rgba(128,128,128, 0.2);">
    </div>

  </div>

  <!-- Right: project description -->

  <div style="flex: 1 1 400px; min-width: 300px; padding-left: 10px;">
    <h3 style="margin-top: 0; margin-bottom: 15px; font-size: 1.4rem; line-height: 1.3; font-weight: 800;">
      CargoForge3D: Multi-GPU Generative 3D Reconstruction Service for Port Breakbulk Cargo Digital Twin Assets
    </h3>


    <div style="margin-bottom: 25px; display: flex; gap: 15px; flex-wrap: wrap;">
      <a href="https://cargo-forge3d.github.io/" style="display: inline-block; background: rgba(0, 123, 255, 0.1); color: #007bff; padding: 6px 12px; border-radius: 4px; text-decoration: none; font-weight: bold; border: 1px solid rgba(0, 123, 255, 0.2); transition: all 0.3s; font-size: 0.9rem;">
        [English Website]
      </a>
      <a href="https://cargo-forge3d.github.io/zh.html" style="display: inline-block; background: rgba(0, 123, 255, 0.1); color: #007bff; padding: 6px 12px; border-radius: 4px; text-decoration: none; font-weight: bold; border: 1px solid rgba(0, 123, 255, 0.2); transition: all 0.3s; font-size: 0.9rem;">
        [中文网站]
      </a>
    </div>
    
    <div style="font-size: 0.95rem; line-height: 1.6; opacity: 0.9; text-align: justify; margin-bottom: 20px;">
      <p style="margin-bottom: 15px;">
        In collaboration with the <strong>Shandong Port Yantai Port Science and Innovation Center</strong>, this project targets rapid mesh asset generation, MB-level model archiving, non-contact cargo acquisition, and real-scale restoration for port breakbulk cargo digital twins. Based on <strong>Tencent Hunyuan3D-2.1</strong>, the system builds an integrated workflow covering image acquisition, generative 3D reconstruction, scale calibration, and digital-twin-ready asset export.
      </p>
      <p style="margin-bottom: 15px;">
        For fast white-mesh generation after crane-triggered image capture, I integrated <strong>HiCache++</strong> into the Shape DiT sampling loop by reusing historical velocity fields and skipping selected DiT forward passes. On an NVIDIA RTX 4080, the 30-step shape sampling time was reduced from <strong>40 s to 7 s</strong>, and the shape end-to-end latency decreased from <strong>67.3 s to 24.0 s</strong>, achieving about <strong>2.8x acceleration</strong> while preserving the downstream mesh pipeline.
      </p>
      <p style="margin-bottom: 15px;">
        To address the 16GB VRAM limit of a single RTX 4080, I designed a <strong>FastAPI + Redis + PostgreSQL</strong> asynchronous serving system with separate shape and texture queues. GPU0 runs a resident white-mesh worker, while GPU1 runs a resident PBR texture worker. The service supports priority scheduling, backpressure, retry/recovery, job auditing, artifact tracking, and resource monitoring. The measured Shape/Texture P95 latencies are <strong>45.4 s / 321.3 s</strong>, corresponding to about <strong>269 textured GLB assets per day</strong> on one dual-4080 node.
      </p>
      <p style="margin-bottom: 0;">
        To improve Hunyuan3D-2.1 on irregular port cargo, I used Hunyuan3D-3.1 as a teacher model to construct <strong>100 real yard-image / high-quality GLB pseudo-label pairs</strong>. After mesh cleaning, watertight conversion, SDF sampling, and multi-view conditional rendering, a <strong>Rank-16 LoRA</strong> domain adaptation was trained for cargo geometry. On the validation set, Chamfer-L1 decreased from <strong>0.0511 to 0.0327</strong> and F-score@0.05 improved from <strong>0.670 to 0.793</strong>.
      </p>
    </div>

  </div>

</div>
<!-- CargoForge3D Project End -->

<hr style="border: 0; border-top: 1px solid rgba(128,128,128, 0.2); margin: 40px 0;">

