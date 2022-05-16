# Robonomics Grant Diary

* **Project Name:** Robossembler
* **Proposal**: [Robossembler Proposal](https://github.com/airalab/robonomics-grant-program/tree/main/proposals/robossembler.md)

---

## Grant Diary no. 19

* **Date**: from 05.03.2022 to 18.03.2022

### Design

* Cubic Modular workspace [alpha v0.1](https://gitlab.com/robosphere/cnc/cubic-modular-workspace/-/commits/v0.1) with Simulation Optimized [3D-Assets](https://gitlab.com/robosphere/cnc/cubic-modular-workspace/-/commit/ed018b11c27bfa03f840e5eb9560175229ea66bf)
* DIY Roboarm [almost prepared](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/935fd877053ef11939d69a683846eb9b526c500b) for alpha version
* Working on Motor Controller PCB

### Programming

* Scene monitor [developement](https://gitlab.com/robosphere/robossembler-ros2/-/commit/67d39432e0a5ec01609f09bac54c4ffd30a40602)

### Simulation

* We are started modeling demonstration scene for Gazebo Simulation with Cubic Modular Workspace and Roboarm DIY version


---

## Grant Diary no. 18

* **Date**: from 20.02.2022 to 04.03.2022

### Design

* 3D-printable Servo Drive [integrated](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/1af246e95dd267f1bf5f58308b60f6e5d80fad8f) to DIY Roboarm

### Programming

* Grasp Pose json export [added](https://gitlab.com/robosphere/forks/ARBench/-/commit/20900e4ebaa28f58a91387fca6284ac6d4364f13). Export format adopted to ROS2 geometry_msgs/Pose

### Simulation

* `Scene monitor` concept introduced. Robossembler ROS2 project will be able to switch between three environment types: `State Ground Truth` with full information about all object in simulation scene from Gazebo or any other engine, `Sensors Simulation` with simulated sensors and `Real Sensors` for running software modules on real hardware. Scene monitor switching beetwen these environment states on a runtime with same control software. With Ignition Gazebo ECS (entity component system) architecture this approach allow to run different simulations in parallel on same machine and combine results for better robot behaviour.

---

## Grant Diary no. 17

* **Date**: from 06.02.2022 to 19.02.2022

### Design

* KiCAD [schematics](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/158d8f253faee8ebb2f1abf305908ea7444ee5cc) for motor control board is ready!
* [Added](https://gitlab.com/robosphere/cnc/cubic-modular-workspace/-/commit/7f4b2992f4d5b46a2e82dee23dc8559224b1db90) first design of edge component for Cubic Modular Workspace

### Programming

* Gripper Support Tool [added](https://gitlab.com/robosphere/forks/ARBench/-/commit/3941c7aae69fc7b448c9cf36ea61e10646323e26) to ARBench
* [Added](https://gitlab.com/robosphere/robossembler-ros2/-/commit/85de7fa68354bbb763f5213f984972f8d5643c46) 3D-printer Behavior Tree Action node

### Simulation

* [Added](https://gitlab.com/robosphere/robossembler-ros2/-/commit/c6df239ae1fdf9cfe5bfb25978d1fd9e11161c5a) `sdf_models` support package for Gazebo models access  


---

## Grant Diary no. 16

* **Date**: from 22.01.2022 to 05.02.2022

### Programming

* [Finished](https://gitlab.com/robosphere/robossembler-ros2/-/commit/dfcc53df09660a7b0b6bf71a544404074483aaad) ROS2 controller for gripper tool and gripper [added](https://gitlab.com/robosphere/robossembler-ros2/-/commit/43c8a363aac1cf7bf01533a63961185a0866cb43) to Plansys2 Behaviour Tree actions
* [Added](https://gitlab.com/robosphere/robossembler-ros2/-/commit/71cfa0991f2ef0c77e5bc3b01c83eef1fcc09716) build job on merge request for Robossembler ROS2 project with Gitlab CI
* Annotation Robotics Workbench (ARBench) [migrated](https://gitlab.com/robosphere/forks/ARBench/-/commit/2111b33c756ee6c473d1300b95fa90921f625a1d) to FreeCAD 0.19 version and merged with freecad_to_gazebo package. It will be used as general purpose tool for export geometric meta-data to simulations from 3D-models.

### Simulation

* [Added](https://gitlab.com/robosphere/robossembler-ros2/-/commit/3d34680aa9a78830c8930e36d8b9e285621d508c) visual meshes for robot manipulator ROS2 support package

---

## Grant Diary no. 15

* **Date**: from 07.01.2022 to 21.01.2022

### Design

* NEW MOTOR! Now is almost fully printed version - [commit](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/0386db9a247b4859f21d02f5ff8453c7f5d1e94a) with image preview
* Manipulator base link or interface part of Cubic Workspace [prepared](https://gitlab.com/robosphere/cnc/cubic-modular-workspace/-/commit/c04fbafa835dc44bcaf19889ec990d2dc2f0a595) for PCB integration
* Cubic workspace scene [preparing](https://gitlab.com/robosphere/cnc/cubic-modular-workspace/-/commit/2d9a68e65ca3a0f85139ac3e52ee97104c6d7561) for simulation 

### Programming

* MoveIt2 & Plansys2 [integration](https://gitlab.com/robosphere/robossembler-ros2/-/commit/8c6b912e00006a26471715d173f4126f2a58170a) - Plansys2 move action for MoveIt
* Added mapping to pddl actions for [assembly sequence](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/f38dbd271aaf463b9bee1b3641c2770b7150c9a7)
* Robossembler ROS2 project with Task & Motion Planning in Gazebo & RViz works for Roboarm-DIY-version and it's Gripper! [Merge-request](https://gitlab.com/robosphere/robossembler-ros2/-/merge_requests/3) with 74 commits

### Simulation

* Optimizing DIY roboarm's [meshes](https://gitlab.com/robosphere/robossembler-ros2/-/commits/add-mesh-visual) for multi-agent simulation performance

### Research

* Added multi-agent planning related [page](https://gitlab.com/robosphere/robossembler-docs/-/commit/d11667bfc02984921004273ef87263bd22a61467)

---

## Grant Diary no. 14

* **Date**: from 23.12.2021 to 06.01.2022

### Design

* Short, more compact & lightweight version of Gripper (branch [smpl-grip-tool](https://gitlab.com/robosphere/arm-tools/grip-tool/-/tree/smpl-grip-tool))
* Passive (without motor) version of [mechanical connection inteface](https://gitlab.com/robosphere/arm-tools/connection-tool/-/commits/passive_connection_tool)
* [Cubic workspace](https://gitlab.com/robosphere/cnc/cubic-modular-workspace) pre-alpha !

---

## Grant Diary no. 13

* **Date**: from 08.12.2021 to 22.12.2021

### Design

* Electrical interface [improved](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/ceece7e5520480bb2286a2f07e4d37f772c3b40f) in diy-roboarm for cordless connectivity
* Cubic [modular workspace](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/ceece7e5520480bb2286a2f07e4d37f772c3b40f) concept ([image](https://gitlab.com/robosphere/cnc/cubic-modular-workspace/-/blob/b067acc246894370a004600dd5d5321a2fa73602/img/cube_v1.png))

### Programming

* [Switched](https://gitlab.com/robosphere/robossembler-ros2/-/commit/f6a18c3c9253e288ecf7cc7dde9dab6b4a48d165) to Behaviour tree action node for planning instead of Moveit MoveGroup interface
* ARBench FreeCAD plugin [ported](https://gitlab.com/robosphere/forks/ARBench/-/commit/c410442b9849dec9299cf403df228c33133a4540) to FreeCAD 0.19 for markup parts in assemblies
* arbench_part_publisher (ROS node for publishing geometric metadata received from FreeCAD with ARBench) [ported](https://gitlab.com/robosphere/forks/arbench_part_publisher/-/commits/foxy-devel) to ROS2 Foxy and tested

### Simulation

* ROS2 project successfully compiled and works with plansys2 and moveit. [README.md](https://gitlab.com/robosphere/robossembler-ros2/-/commit/cece8b24aa55f110267d3dab645624b374e3363d) manual tested for reproduce

### Research

* [Graph-database overview](https://gitlab.com/robosphere/robossembler-docs/-/commit/3a792cfabbffcd2dbd722ae86862869c3cb5c86e) for robossembler knowledge database

---

## Grant Diary no. 12

* **Date**: from 23.11.2021 to 07.12.2021

### Design

* [Version 0.3](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/ca54b5aae0c190d4bc3e471d8c1d2011d3e0ce92) of diy-robot-manipulator
* Added [calculation report](https://gitlab.com/robosphere/roboarm-diy-version/-/blob/91a1a993ab132887202ebb202b59538f2bb2a8fc/calc/Mathcad%20-%20reduce.pdf) for gearbox
* Grip-tool branched into [rotatable](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commits/rotatable-grip-tool-v3.1) (with 2 motors) and short (with 1 motor) version. To short version [added](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commit/881ad0213f969db3686923eca981197923f8337d) PCB interfaces
* Controller board schematics [released](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/d9effed223942346aee5261826abccd5377944f3) ([pdf](https://gitlab.com/robosphere/roboarm-diy-version/-/blob/d9effed223942346aee5261826abccd5377944f3/motor_module.pdf)) in open source EDA KiCAD format

### Programming

* In Plansys2 & MoveIt2 integration added [first draft](https://gitlab.com/robosphere/robossembler-ros2/-/commit/dffd9816bd5d407f652fcca2010d947df9984e30)

---

## Grant Diary no. 11

* **Date**: from 08.11.2021 to 22.11.2021

### Design

* Updated interfaces for [molded Roboarm](https://gitlab.com/robosphere/roboarm/-/commit/7a7215f2ea0ae75bd6c07b1ae726e9ff5aa52cda) and [hexagonal workspace](https://gitlab.com/robosphere/cnc/roboarm-workspace/-/commit/68a742f06bdc71d38350f31469742930f1f2ecb4)
* Updated connection interface for [grip tool](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commit/c64900ac6a5d3c87658feaccf3df85d6723f09d3) and [other improvements](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commit/d84823e11a3e1f44801669f7ba78196ed2bd5618)
* First [schematic design](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/82f42159e0942b1277111a14512fb040b5dfb588) of motor controller board
* Improved [hexagonal workspace interface](https://gitlab.com/robosphere/cnc/roboarm-workspace/-/commit/de8118fe45ebac220cf98bc68a6754d82cc5b622)
* Updated [Gearbox](https://gitlab.com/robosphere/robossembler-ros2/-/commit/88fc464fafeac93e99b35419bcbe79cd8c6a8da9) for DIY-manipulator

### Programming

* Started MoveIt2 and Plansys2 integration

### Simulation

* Updated [robot description package](https://gitlab.com/robosphere/robossembler-ros2/-/commit/dfaea654f1160fb16f69fa5bdbc3eed5b6cbdb15) with URDF and configs
* Added [simplified STEP-model](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/c3498fa3f36aef00ef128459721192df6173c93a) of DIY-manipulator
* Added [camera interface](https://gitlab.com/robosphere/robossembler-ros2/-/commit/88fc464fafeac93e99b35419bcbe79cd8c6a8da9) in Gazebo simulation


---

## Grant Diary no. 13

* **Date**: from 08.12.2021 to 22.12.2021

### Design

* Electrical interface [improved](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/ceece7e5520480bb2286a2f07e4d37f772c3b40f) in diy-roboarm for cordless connectivity
* Cubic [modular workspace](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/ceece7e5520480bb2286a2f07e4d37f772c3b40f) concept ([image](https://gitlab.com/robosphere/cnc/cubic-modular-workspace/-/blob/b067acc246894370a004600dd5d5321a2fa73602/img/cube_v1.png))

### Programming

* [Switched](https://gitlab.com/robosphere/robossembler-ros2/-/commit/f6a18c3c9253e288ecf7cc7dde9dab6b4a48d165) to Behaviour tree action node for planning instead of Moveit MoveGroup interface
* ARBench FreeCAD plugin [ported](https://gitlab.com/robosphere/forks/ARBench/-/commit/c410442b9849dec9299cf403df228c33133a4540) to FreeCAD 0.19 for markup parts in assemblies
* arbench_part_publisher (ROS node for publishing geometric metadata received from FreeCAD with ARBench) [ported](https://gitlab.com/robosphere/forks/arbench_part_publisher/-/commits/foxy-devel) to ROS2 Foxy and tested

### Simulation

* ROS2 project successfully compiled and works with plansys2 and moveit. [README.md](https://gitlab.com/robosphere/robossembler-ros2/-/commit/cece8b24aa55f110267d3dab645624b374e3363d) manual tested for reproduce

### Research

* [Graph-database overview](https://gitlab.com/robosphere/robossembler-docs/-/commit/3a792cfabbffcd2dbd722ae86862869c3cb5c86e) for robossembler knowledge database

---

## Grant Diary no. 12

* **Date**: from 23.11.2021 to 07.12.2021

### Design

* [Version 0.3](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/ca54b5aae0c190d4bc3e471d8c1d2011d3e0ce92) of diy-robot-manipulator
* Added [calculation report](https://gitlab.com/robosphere/roboarm-diy-version/-/blob/91a1a993ab132887202ebb202b59538f2bb2a8fc/calc/Mathcad%20-%20reduce.pdf) for gearbox
* Grip-tool branched into [rotatable](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commits/rotatable-grip-tool-v3.1) (with 2 motors) and short (with 1 motor) version. To short version [added](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commit/881ad0213f969db3686923eca981197923f8337d) PCB interfaces
* Controller board schematics [released](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/d9effed223942346aee5261826abccd5377944f3) ([pdf](https://gitlab.com/robosphere/roboarm-diy-version/-/blob/d9effed223942346aee5261826abccd5377944f3/motor_module.pdf)) in open source EDA KiCAD format

### Programming

* In Plansys2 & MoveIt2 integration added [first draft](https://gitlab.com/robosphere/robossembler-ros2/-/commit/dffd9816bd5d407f652fcca2010d947df9984e30)

---

## Grant Diary no. 11

* **Date**: from 08.11.2021 to 22.11.2021

### Design

* Updated interfaces for [molded Roboarm](https://gitlab.com/robosphere/roboarm/-/commit/7a7215f2ea0ae75bd6c07b1ae726e9ff5aa52cda) and [hexagonal workspace](https://gitlab.com/robosphere/cnc/roboarm-workspace/-/commit/68a742f06bdc71d38350f31469742930f1f2ecb4)
* Updated connection interface for [grip tool](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commit/c64900ac6a5d3c87658feaccf3df85d6723f09d3) and [other improvements](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commit/d84823e11a3e1f44801669f7ba78196ed2bd5618)
* First [schematic design](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/82f42159e0942b1277111a14512fb040b5dfb588) of motor controller board
* Improved [hexagonal workspace interface](https://gitlab.com/robosphere/cnc/roboarm-workspace/-/commit/de8118fe45ebac220cf98bc68a6754d82cc5b622)
* Updated [Gearbox](https://gitlab.com/robosphere/robossembler-ros2/-/commit/88fc464fafeac93e99b35419bcbe79cd8c6a8da9) for DIY-manipulator

### Programming

* Started MoveIt2 and Plansys2 integration

### Simulation

* Updated [robot description package](https://gitlab.com/robosphere/robossembler-ros2/-/commit/dfaea654f1160fb16f69fa5bdbc3eed5b6cbdb15) with URDF and configs
* Added [simplified STEP-model](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/c3498fa3f36aef00ef128459721192df6173c93a) of DIY-manipulator
* Added [camera interface](https://gitlab.com/robosphere/robossembler-ros2/-/commit/88fc464fafeac93e99b35419bcbe79cd8c6a8da9) in Gazebo simulation


---

## Grant Diary no. 10

* **Date**: from 24.10.2021 to 07.11.2021

### Design

* Transport Module [updated](https://gitlab.com/robosphere/transport-module/-/commit/6c91ef2615cebb240df3c89797f5f92f3972a72f)
* Gripper [optimized](https://gitlab.com/robosphere/arm-tools/grip-tool/-/merge_requests/6) for automatic assembly and some other improvements, [added](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commits/8-simple-construction-grip-tool) short version 
* Published [sources](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/6ef4b6f6ddde26f146c227a94a6038a383e97d88)  for Topoligical Optimized 3D-printed Robot-manipulator

### Programming

* Working scene with ROS2 & MoveIt2
* Fixed [textures](https://gitlab.com/robosphere/ignition-fuel-export/-/merge_requests/7) in SDF-package for Ignition Fuel Exporter

### Simulation

* Started test integration ROS2 & Unity with Unity-Robotics-Hub or other middleware packages - ROS-for-Unity, DDS-for-Unity. Gazebo isn't suitable for multi-agent systems. Now we decide to simulate small manipulation tasks in Gazebo and Unity for multi-agent scenarios.

### Research

* We have started to prepare publication for IEEE with architecture of Robossembler & Robonomics integration
* Published San Diego UC Assembly Challenge 2020 Paper's [overview](https://robosphere.gitlab.io/robossembler-docs/docs/technologies/wrs2020-assembly-challenge#%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82-%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D1%8B-uc-san-diego)


---

## Grant Diary no. 9

* **Date**: from 09.10.2021 to 23.10.2021

### Design

* Published second version of [Transport module](https://gitlab.com/robosphere/transport-module/-/commit/d902a3a0d1c672c099de88c49b525279a5ad5be7) with README
* [Connector interface](https://gitlab.com/robosphere/arm-tools/connection-tool) version 4, now it's symmetric!
* [Gripper](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commit/105af0651ca4bce28df70af55612eb39db69d3ce) became more stable
* [Published](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/bd3d4f472fcbab190ba8409a60c167f1030ac50a) 3D-printing Robot-manipulator. Successfully finished topological optimisation of this version and it will be released in next 2 weeks

### Programming

* [Ignition Fuel Export plugin](https://gitlab.com/robosphere/ignition-fuel-export) - added pythonocc support, improved composability, added preview of assemblies in Ignition Fuel packages

### Simulation

* Published [assembly plan's draft](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/76fe047426745f05c3fd618fd5420b626dbeea6e) for 3D-printing Robot-manipulator
* We [have started](https://gitlab.com/robosphere/robossembler-ros2/-/commits/dev-motion-planning-ignition-gazebo) Ignition Gazebo integration

### Research

* Assembly Sequence Planning State-of-the-Art [overview](https://robosphere.gitlab.io/robossembler-docs/docs/technologies/ASP-overview)


---

## Grant Diary no. 8

* **Date**: from 25.09.2021 to 08.10.2021

[New index page](https://robosphere.gitlab.io/robossembler-docs/docs/) with links to all project repos.

### Design

* New [post-processing tool](https://gitlab.com/robosphere/arm-tools/post-processing-tool) - lightweight alternative to classic CNC-machines for milling
* New [scanning tool](https://gitlab.com/robosphere/arm-tools/scan-tool)
* Updated [welding tool](https://gitlab.com/robosphere/arm-tools/welding-tool)

### Programming

* [Ignition Fuel Export plugin](https://gitlab.com/robosphere/ignition-fuel-export) alpha release

### Research

* [Assembly Challenge Project from o2ac team](https://robosphere.gitlab.io/robossembler-docs/docs/technologies/o2ac-repo-review) overview
* [Plansys2 framework](https://robosphere.gitlab.io/robossembler-docs/docs/technologies/plansys2) overview

---

## Grant Diary no. 7

* **Date**: from 10.09.2021 to 24.09.2021

### Design

* New [extrude&melt tool](https://gitlab.com/robosphere/arm-tools/extrude-melt-tool)
* Published DIY-roboarm [version 2](https://gitlab.com/robosphere/roboarm-diy-version/-/commit/ba67f3ca1eaadc4fcedd677380c4462f730379e4)
* Updated [gripper-tool](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commit/a3a3e83c06fc2b46fbdb2bda97de6a1444f6c31f)
* We make decision to unify our robots and instead of creating separate transporter we will create wheel-modules to workspaces

### Programming

* We have started to develope [python-package](https://gitlab.com/robosphere/ignition-fuel-export) to automate CAD -> Ignition Fuel export
* [Started](https://gitlab.com/robosphere/roboarm/-/issues/4) Ignition Gazebo integration with ROS and our CAD-models

### Research

* We have found solution to replace classic CNC for CNC-based operations - milling, etc. It will be presented in near future

---


## Grant Diary no. 6

* **Date**: from 26.08.2021 to 09.09.2021

### Design

* [Version 3](https://gitlab.com/robosphere/arm-tools/connection-tool/-/commit/6a2c4309b73d45977495bc7879f55477e2cb8024) of connection tool (interface)
* Published [soldering cartridge](https://gitlab.com/robosphere/arm-tools/solder-cartridge/-/commit/89f0e2bb8b8c0c955a8941743d996f3df65d3eb4) for soldering tool
* Updated [gripper-tool](https://gitlab.com/robosphere/arm-tools/connection-tool/-/commit/6a2c4309b73d45977495bc7879f55477e2cb8024). Work in progress
* A model of a CNC machine is being developed, parts of which can be manufactured on it itself

### Research

* We investigate advanced techniques for processing and separating substances from industrial and household waste. These technologies may be required to find an affordable and profitable way for a robot factory to extract resources not only from natural sources, but also from the technosphere. A report on this work will be published soon.
* Several scenarios for integrating the Robossembler project with the Robonomics Network have been developed. They are currently being coordinated with the Robonomics team.


---

## Grant Diary no. 5

* **Date**: from 12.08.2021 to 25.08.2021

### Design

* Published robossembler's unique [5-axis CNC](https://gitlab.com/robosphere/cnc/5-axis-cnc/-/commit/64c0cccec28701ebb6ab639c788e5cf799789924), that will be used in manufactoring parts of roboarm
* Published detailed version of our [roboarm](https://gitlab.com/robosphere/roboarm/-/commit/609efe7ee400e81a2e5ee4066dde684731a8d91e)
* Published [mold](https://gitlab.com/robosphere/cnc/roboarm-link-mold/-/commit/5aeb83a9687e925d8cc73f9d0f8234017fd54e00) for roboarm link manufactoring
* Published updated version of [workspace](https://gitlab.com/robosphere/cnc/roboarm-workspace/-/commit/4ea13cfe3fac381ef10bc6b9089eef998db51870) for roboarm
* Updated [connection tool](https://gitlab.com/robosphere/arm-tools/connection-tool/-/commit/b35a9a9a0155088bf90e62350869f0f08561b7ad)
* Updated [gripper tool](https://gitlab.com/robosphere/arm-tools/grip-tool/-/commit/899cc0c226658d2b8d296c76f9dd2c39e9c0207b)


### Research

* I have found very interesting EU grant research project [PERFoRM](https://cordis.europa.eu/project/id/680435). One of results in this research - comparison of different manufactoring data interchange formats, that leads to develope another format - PERFoRMML ([specification](https://ec.europa.eu/research/participants/documents/downloadPublic?documentIds=080166e5afcc224f&appId=PPGMS)). It will help for us with choosing standartized way to data-exchange with CNC, roboarms and another CPS in Robossembler.
* Added some useful tools in our [awesome-open-source-robotics list](https://gitlab.com/robosphere/open-source-robotics-projects/-/commit/e9ddc1be7efc2590acb2e6831c244fec0785b430)

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
