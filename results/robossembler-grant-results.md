# Robonomics Grant Results

* **Project Name:** Robossembler
* **Proposal**: https://github.com/airalab/robonomics-grant-program/blob/main/proposals/robossembler.md
* **Grant Diary**: https://github.com/airalab/robonomics-grant-results/blob/main/diaries/robossembler-grant-diary.md

| No. | Deliverable | Link | Notes |
|:---:|:-----------:|:----:|:-----:|
|  1  | 3D-printed 6-axis robot-manipulator without fasteners | [git](https://gitlab.com/robosphere/roboarm-diy-version) | [CAD models](https://gitlab.com/robosphere/roboarm-diy-version/-/tree/main/src), [schematics/PCB](https://gitlab.com/robosphere/roboarm-diy-version/-/tree/main/brd), [mech math report](https://gitlab.com/robosphere/roboarm-diy-version/-/blob/main/calc/Mathcad%20-%20reduce.pdf) |
|  2  | Molded 6-axis robot-manipulator without fasteners | [git](https://gitlab.com/robosphere/roboarm) |  [link mold](https://gitlab.com/robosphere/cnc/roboarm-link-mold) for link manufactoring, [servo drive](https://gitlab.com/robosphere/servo) |
|  3  | Modular components for creating customized cubic workspaces | [git](https://gitlab.com/robosphere/cnc/cubic-modular-workspace) | [Blender assets](https://gitlab.com/robosphere/cnc/cubic-modular-workspace/-/tree/main/blender-assets) ([demo-video](https://www.youtube.com/watch?v=sJLnEXayEq4)) |
|  4  | Modular components for creating customized hexagonal workspaces | [git](https://gitlab.com/robosphere/cnc/roboarm-workspace) | [transport module](https://gitlab.com/robosphere/transport-module) for transform hexagonal workspace into Robot-transporter |
|  5  | Tools for robot-manipulator | [git](https://gitlab.com/robosphere/arm-tools) | Ready for prototype manufactoring: [grip tool](https://gitlab.com/robosphere/arm-tools/grip-tool); Proof of Concept: [soldering tool](https://gitlab.com/robosphere/arm-tools/soldering-tool), [print tool](https://gitlab.com/robosphere/arm-tools/3d-print-tool), [extrude melting tool](https://gitlab.com/robosphere/arm-tools/extrude-melt-tool), [welding tool](https://gitlab.com/robosphere/arm-tools/welding-tool) |
|  6  | Classic 5-axis-CNC | [git](https://gitlab.com/robosphere/cnc/5-axis-cnc) |  ...  |
|  7  | Annotation Robotics Workbench |  [git](https://gitlab.com/robosphere/forks/ARBench) | A FreeCAD workbench for annotating frames and exporting part information into Robotics simulator with our additional features: gripper positioning and exporting SDF-packages to Gazebo simulator or [Ignition Fuel Server](https://gitlab.com/robosphere/ignition-fuel-export) |
|  8  | Robossembler ROS2 Package Set | [git](https://gitlab.com/robosphere/robossembler-ros2) | [Robonomics support](https://gitlab.com/robosphere/robossembler-ros2/-/tree/main/robonomics) for launching manufactoring plan from blockchain ([demo-video](https://www.youtube.com/watch?v=J3m5hXf-cro)), [Robot-manipulator support](https://gitlab.com/robosphere/robossembler-ros2/-/tree/main/rasmt_support), [Task & motion planning](https://gitlab.com/robosphere/robossembler-ros2/-/tree/main/robossembler) with Plansys2 and Moveit2, [Scene monitor](https://gitlab.com/robosphere/robossembler-ros2/-/tree/main/robossembler_scene_monitor) for switching between Simulation and Real Worlds |
|  9  | Research Docs (RU) | [git](https://gitlab.com/robosphere/robossembler-docs), [web](https://robosphere.gitlab.io/robossembler-docs/docs/) | [Open Source Robotics](https://gitlab.com/robosphere/robossembler-docs/-/blob/89d9d2df878049a941371eb29103e45e47316304/docs/technologies/open-source-robots-and-tools.md), [Machine Learning in Robotics](https://gitlab.com/robosphere/robossembler-docs/-/blob/89d9d2df878049a941371eb29103e45e47316304/docs/technologies/machine-learning-in-robotics.md), [Assembly Sequence Planning](https://gitlab.com/robosphere/robossembler-docs/-/blob/89d9d2df878049a941371eb29103e45e47316304/docs/technologies/assembly-sequence-planning-overview.md), [Assembly Challenge'2020 Projects](https://gitlab.com/robosphere/robossembler-docs/-/blob/89d9d2df878049a941371eb29103e45e47316304/docs/technologies/wrs2020-assembly-challenge.md), [Papers]() |