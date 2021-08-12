# Robonomics Grant Diary

* **Project Name:** Robossembler
* **Proposal**: [Robossembler Proposal](https://github.com/airalab/robonomics-grant-program/tree/main/proposals/robossembler.md)

---

## Grant Diary no. 4

* **Date**: from 29.07.2021 to 11.08.2021

### Design

* v0.1 [library for storing tools](https://gitlab.com/robosphere/arm-tools/tools-library/-/commit/4149cccd652b6c0932685d2465334b9adb38c27e)
* Released [DIY version of our robot-manipulator](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/5a9e667ef7e2fe21dbf4c1e38dc590999e39e71b) with cheap mass market servos
* v3 [connection tool](https://gitlab.com/robosphere/arm-tools/connection-tool/-/commit/2f989306f03a8ad18993c840926bc8f8171beb84)
* Gripper tool still under developement
* Started functional electric schematics of roboarm workspace (manipulator + tools)

### Research

* We started to explore Open Cascade Technology (OCCT) - industrial quality open source geometric core (C++ library) for CAD systems (FreeCAD is based on that). OCCT with be used to analyse/decompose assemblies for assembly task management automation and model reuse.

---

## Grant Diary no. 3

* **Date**: from 15.07.2021 to 28.07.2021

### Design

* Released 3rd version of [connection tool](https://gitlab.com/robosphere/arm-tools/connection-tool)
* Published 1st version of [extruder tool](https://gitlab.com/robosphere/arm-tools/extrude-melt-tool) for compound extruding
* Still under developement [gripper tool](https://gitlab.com/robosphere/arm-tools/grip-tool). Task is very challenging because we need tool, that can be simply assembled with same grippers without programming complexity overhead

### Technology

* Founded new material for roboarm link - [Furfural Resin](https://gitlab.com/robosphere/robossembler-docs/-/issues/3#note_635775190), that is maded from wood

### Simulation

* Published first version of [Unreal Engine Project](https://gitlab.com/robosphere/robossembler-unreal-engine-project) with two basic scenes
  * `robot arm assembly line` - for assembly simulation with CAD-exported models of tools, arms, CNC's
  * `self replicated factory` - for replication simulation with abstract blocks - created during online [VR-modeling sessions](https://www.youtube.com/playlist?list=PLTch2Mxp-At8FouCLnO5gBmhlm-VwQ6fH)

### Research

* Research of RL in robotic arm manipulation applications are finished [article](https://robosphere.gitlab.io/robossembler-docs/docs/technologies/machine-learning-in-robotics)
* Started research of 3D-formats to automated extract CAD-models to packages for manufactoring


---

## Grant Diary no. 2

* **Date**: from 01.07.2021 to 14.07.2021

### Design

* Released first designs of [3D-print tool](https://gitlab.com/robosphere/arm-tools/3d-print-tool), [connection tool](https://gitlab.com/robosphere/arm-tools/connection-tool)(tool for connect other tools to manipulator)
* Released improved versions of [soldering](https://gitlab.com/robosphere/arm-tools/soldering-tool) and [welding](https://gitlab.com/robosphere/arm-tools/welding-tool) tools
* [Started](https://gitlab.com/robosphere/arm-tools/grip-tool/-/issues/1) design mechanical gripper tool with [overview](https://robosphere.gitlab.io/robossembler-docs/docs/technologies/gripper-tools-research) of currently existed models

### Research

* Published [research](https://robosphere.gitlab.io/robossembler-docs/docs/mining) of possible approached to mine resources in self-replicated industrial systems. This work partly visualized in session of Gravity Sketch VR-modeling (not ready for publish yet)
* We are still searching for a modern state-of-the-art approaches to automating robot programming through reinforcement learning. The results are published in the [article](https://robosphere.gitlab.io/robossembler-docs/docs/technologies/machine-learning-in-robotics). Over the next two weeks, we plan to complete the selection of tools and approaches for programming Robossembler agents and begin to implement them in code.


---

## Grant Diary no. 1

* **Date**: from 01.04.2021 to 01.07.2021

### Design

* [Robot arm Welding Tool](https://gitlab.com/robosphere/arm-tools/welding-tool)
* [Robot arm Soldering Tool](https://gitlab.com/robosphere/arm-tools/soldering-tool)
* [Robot Arm URDF model](https://gitlab.com/robosphere/roboarm)
* [Servo](https://gitlab.com/robosphere/servo)

### Research

* [Generative Design Model of Self-Replicated Cell](https://gitlab.com/robosphere/robossembler-docs/-/blob/master/docs/models/generation)
* [Cells Growth Model](https://gitlab.com/robosphere/robossembler-docs/-/tree/master/docs/models/growth)
* [Open Source Robot Arm Compilation](https://gitlab.com/robosphere/open-source-robotics-projects)
* [Automatic storage and transportation of objects concept](https://gitlab.com/robosphere/robossembler-docs/-/blob/master/docs/autostorage.md)
* [Road to Self-Replicated Manufactoring](https://gitlab.com/robosphere/robossembler-docs/-/blob/master/docs/replication.md)
* [Control System of Self-Replicated Systems](https://gitlab.com/robosphere/robossembler-docs/-/blob/master/docs/information/information_support.md)

### Technology

* [Robot Arm Assembly Workflow](https://gitlab.com/robosphere/robossembler-docs/-/blob/master/docs/techinstruction.md)
* [Wood as Multipurpose Raw Material for Self-Replicated Manufactoring](https://gitlab.com/robosphere/robossembler-docs/-/blob/master/docs/technologies/wood.md)
