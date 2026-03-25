---
layout: page
permalink: /research/
title: research
description: Robot Perception and Learning (RoPAL)
nav: true
---

<div class="row">
  <div class="col-sm-4 mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/kukaiiwa.png' | relative_url }}" alt="Robot manipulation platform"
     style="width: 100%; height: 220px; object-fit: contain; display: block; background: #f5f5f5;" />
    </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/youbot.png' | relative_url }}" alt="Mobile robot platform"    
     style="width: 100%; height: 220px; object-fit: contain; display: block; background: #f5f5f5;" />
  </div>
</div>

## Overview

My research is centred on **Robot Perception and Learning (RoPAL)**, with the aim of building autonomous robotic systems that can sense, understand, and act robustly in real-world environments. Across mobile robotics, robot manipulation, sensing, and smart manufacturing, the common theme is to combine rich perception with continuous learning so that robots can operate beyond tightly scripted laboratory settings.

I have worked across academia and industry on indoor mobile robots, industrial robot manipulators, humanoid and service robots, and outdoor unmanned autonomous surface vehicles. That background continues to shape the group’s work: we pursue fundamental advances in robotics and AI, but always with deployment, safety, and industrial relevance in view.

Current work spans:

- deep reinforcement learning for navigation and manipulation
- differentiable physics and physics-informed learning for robotics
- state estimation, including visual SLAM and visual odometry
- sensor-guided autonomous navigation and manipulation
- multi-modal robot sensing, including vision, tactile sensing, lidar, and smart sensors
- computer vision and data-driven methods for smart manufacturing, surface metrology, and robotic assembly

## Research Directions

### Differentiable Physics and Physics-Informed Robot Learning

A growing research direction in the group is **differentiable physics for robotic manipulation**, especially for materials and environments that are difficult to model with conventional rigid-body assumptions. The motivation is straightforward: many real manipulation tasks involve granular, deformable, or elastoplastic materials, where purely data-driven learning is expensive and often unstable, while purely analytical modelling is too restrictive.

Our recent work explores how differentiable physics and physics-informed learning can provide a more useful middle ground by combining model structure with learning-based adaptation. This enables robots to reason about material behaviour, improve system identification, and learn manipulation strategies more efficiently for tasks where interaction dynamics matter.

Representative recent publications in this direction include:

- [*DDBot: Differentiable Physics-Based Digging Robot for Unknown Granular Materials*](https://doi.org/10.1109/TRO.2025.3636815)
- [*Differentiable physics-based system identification for robotic manipulation of elastoplastic materials*](https://doi.org/10.1177/02783649251334661)
- [*A Physics-Informed Demonstration-Guided Learning Framework for Granular Material Manipulation*](https://doi.org/10.1109/TNNLS.2025.3622482)

Together, these works define a research programme focused on physically grounded robot learning: using differentiable models, demonstrations, and data-driven updates to improve manipulation performance on challenging real materials rather than only on simplified benchmark tasks.

<div class="row align-items-stretch">
  <div class="col-md-6 mt-3 mt-md-0 d-flex">
    <div class="w-100">
      <a href="https://doi.org/10.1109/TRO.2025.3636815" target="_blank" rel="noopener noreferrer">
        <img
          class="img-fluid rounded z-depth-1"
          src="https://moonlight-paper-snapshot.s3.ap-northeast-2.amazonaws.com/arxiv/ddbot-differentiable-physics-based-digging-robot-for-unknown-granular-materials-2.png"
          alt="DDBot paper figure"
          style="width: 100%; height: 180px; object-fit: contain; display: block; background: #f5f5f5;"
        />
      </a>
      <p class="text-center mt-2 mb-0">
        <a href="https://doi.org/10.1109/TRO.2025.3636815" target="_blank" rel="noopener noreferrer">DDBot</a>
      </p>
    </div>
  </div>
  <div class="col-md-6 mt-3 mt-md-0 d-flex">
    <div class="w-100">
      <a href="https://doi.org/10.1177/02783649251334661" target="_blank" rel="noopener noreferrer">
        <img
          class="img-fluid rounded z-depth-1"
          src="https://figures.semanticscholar.org/ecb4e5f3df4865b7299c3a7d1528f9768d4bd356/2-Figure1-1.png"
          alt="Differentiable physics system identification paper figure"
          style="width: 100%; height: 180px; object-fit: contain; display: block; background: #f5f5f5;"
        />
      </a>
      <p class="text-center mt-2 mb-0">
        <a href="https://doi.org/10.1177/02783649251334661" target="_blank" rel="noopener noreferrer">Differentiable physics-based system identification</a>
      </p>
    </div>
  </div>
</div>

### Autonomous Navigation, SLAM, and Robot Perception

We develop perception pipelines that improve localisation, mapping, scene understanding, and active decision-making for mobile robots and autonomous systems. The emphasis is on robust autonomy in challenging, dynamic, or partially observable environments, combining vision, lidar, GNSS, and learned representations with decision-making that remains effective beyond carefully structured benchmark settings.

Recent work in this direction includes hierarchical reinforcement learning for mapless navigation with Predictive Neighbouring Space Scoring (PNSS), where compact predicted explorable-space representations support long-horizon subgoal selection, and GNSS-aware autonomy in urban environments, where lidar-based LOS/NLOS classification and reflection-path reasoning help analyse and mitigate non-line-of-sight effects. Together, these projects reflect a broader interest in making robot perception more actionable: not only estimating the environment, but improving navigation reliability under sparse rewards, perceptual ambiguity, and real-world sensing distortions.

<div class="row align-items-stretch">
  <div class="col-md-8 mt-3 mt-md-0 d-flex">
    <div class="w-100">
      <div class="row">
        <div class="col-sm-6 mt-3 mt-md-0">
          <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/PNSS_Fig1.gif' | relative_url }}" alt="PNSS figure 1" />
        </div>
        <div class="col-sm-6 mt-3 mt-md-0">
          <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/PNSS_Fig2.gif' | relative_url }}" alt="PNSS figure 2" />
        </div>
      </div>
      <p class="text-center mt-2 mb-0">
        <a href="https://doi.org/10.1109/TASE.2023.3312237" target="_blank" rel="noopener noreferrer">PNSS framework and predicted neighbouring space scoring</a>
      </p>
    </div>
  </div>
  <div class="col-md-4 mt-3 mt-md-0 d-flex">
    <div class="w-100">
      <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/GNSS_data.gif' | relative_url }}" alt="GNSS NLOS figure 1" />
      <p class="text-center mt-2 mb-0">
        <a href="https://doi.org/10.1109/ICAC65379.2025.11196430" target="_blank" rel="noopener noreferrer">GNSS NLOS mitigation in urban navigation</a>
      </p>
    </div>
  </div>
</div>

### Robot Manipulation and Reinforcement Learning

Another major direction is self-learning robot manipulation. We study how robots can acquire robust behaviours for grasping, rearrangement, and multi-step interaction in cluttered and uncertain environments, especially where hand-crafted control logic becomes brittle or impractical.

This includes reinforcement learning for navigation and manipulation, vision-guided manipulation, and recent work on differentiable and physics-informed learning for interaction with granular, viscous, and elastoplastic materials. A recurring research question is how to bridge the gap between elegant lab demonstrations and manipulation systems that remain reliable in practice.

<div class="row">
  <div class="col-sm-6 mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/rl_robot1.png' | relative_url }}" alt="Robot learning" />
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/rl_robot.png' | relative_url }}" alt="Robot manipulation research" />
  </div>
</div>

### Multi-Modal Sensing and Smart Manufacturing

We also work on sensing-rich robotic systems for manufacturing and inspection. This includes robot-based photometric stereo, large-scale 3D surface imaging, defect monitoring, and data-driven quality assessment for manufacturing processes.

A representative thread in this area is selective laser melting and laser powder bed fusion monitoring, where visual and data-driven methods can help identify process anomalies and improve manufactured part quality. Related work also includes self-validating and self-diagnosing sensing systems that recover from corrupted measurements using learning-based approaches.

<div class="row">
  <div class="col-sm-6 mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/ps1.png' | relative_url }}" alt="Robot-based surface metrology" />
  </div>
  <div class="col-sm-3 mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/layout0620_n.jpg' | relative_url }}" alt="Manufacturing monitoring" />
  </div>
  <div class="col-sm-3 mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/self_validate.png' | relative_url }}" alt="Self-validating sensing" />
  </div>
</div>

### Autonomous Vehicles and Field Robotics

My work also includes autonomous vehicles and multi-robot systems, including unmanned surface vehicles and UAV-related systems. These projects connect perception, state estimation, control, and sensor fusion with real hardware deployment.

This line of work reflects a broader interest in embodied autonomy: robots and vehicles must reason under uncertainty, coordinate across sensing channels, and operate safely outside idealised test conditions.

<div class="row">
  <div class="col-sm-4 mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/IMG_6562.jpg' | relative_url }}" alt="USV project" />
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/IMG_6563.jpg' | relative_url }}" alt="Autonomous vehicle project" />
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/IMG_6565.jpg' | relative_url }}" alt="Student vehicle platform" />
  </div>
</div>

## Selected Grants and Projects

The following grants and projects reflect the current research portfolio presented on my Cardiff profile.

| Sponsor | Project | Role | Value | Duration |
| --- | --- | --- | --- | --- |
| UKRI BBSRC | Agriculture Living Machine of Operatable Nano-Droplets (ALMOND) | Co-I for robotics and autonomous systems | £1.6M total | 2024-2026 |
| Royal Academy of Engineering | Visiting Professor for Raphael Grech (Spirent) | Academic Champion | £30,000 | Sep 2023 - Sep 2026 |
| DTII, Cardiff University | Enhancing Autonomous Systems with Multi-Modal Sensor-based Environment Digitalisation: Ensuring Safety, Security, and Reliability | PI | £4,000 | Jun 2023 - Jul 2023 |
| EPSRC DTP | Robot Learning for Manipulation | PI | £76,000 | Oct 2023 - Apr 2027 |
| Royal Academy of Engineering | Active Perception and Learning for Autonomous Navigation | Industrial Fellowship | £50,000 | Sep 2022 - Sep 2024 |
| EPSRC New Horizons | PHYDL: Physics-informed Differentiable Learning for Robotic Manipulation of Viscous and Granular Media | PI / Co-investigator with Yukun Lai | £250k | Jan 2023 - Jun 2025 |
| SmartExpertise | DIGIBRIDGE: Physics-informed digital twin supported smart bridge maintenance | Co-I | £111,884 | Nov 2021 - Dec 2022 |
| Innovate UK / KTP | BIM and Digital Twins in support of Smart Bridge Structural Surveying | Co-I, Knowledge Supervisor | £280,000 | Sep 2021 - Sep 2024 |
| Industry (Spirent) | Reinforcement Learning for autonomous navigation with GNSS-based localisation | PI | £32,000 | 2021 - 2024 |
| Royal Society | Active Robot Learning for Subtractive, Formative, and Additive Manipulations of Granular and Viscous Materials | PI | £17,812 | 09 Mar 2020 - 08 Mar 2021 |

## Research Context

My current research environment sits at the intersection of robotics, computer vision, machine learning, smart sensing, and manufacturing. The intention is to use advanced perception and learning not as isolated algorithmic components, but as integrated capabilities that support autonomous navigation, dexterous manipulation, inspection, monitoring, and human-centred industrial systems.

Much of this work is shaped by real deployment constraints: sensing uncertainty, model mismatch, limited supervision, safety requirements, and the need to transfer methods from simulation and controlled experiments to real robotic platforms. That is why the group’s work repeatedly returns to a common question: how can robots learn effectively while remaining grounded in physical interaction, rich sensing, and task-level reliability?
