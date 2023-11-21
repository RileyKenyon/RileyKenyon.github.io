---
layout: page
title: Resume
external_url: /img/2019/Resume_Website_KenyonRiley.pdf 
permalink: /resume/
---
<!-- <link rel="stylesheet" href="https://raw.githubusercontent.com/markdowncss/retro/master/css/retro.css"> -->
# Riley Kenyon
Broomfield, CO, USA • Riley.Kenyon@colorado.edu • 303-330-5684 • [rileykenyon.github.io](https://rileykenyon.github.io) • [pdf](/img/2019/Resume_Website_KenyonRiley.pdf)

## EDUCATION

#### M.S. Mechanical Engineering, University of Colorado Boulder May 2020
- GPA: 3.97/4.0

#### B.S. Mechanical Engineering, University of Colorado Boulder May 2019
- GPA: 3.85/4.0

#### Certificates:
- University of Toronto Self Driving Vehicle
- Certified SolidWorks Associate (C-33LVZSD55F)
- NVIDIA Fundamentals of Accelerated Computing with CUDA C/C++
- STK level 1 Certified

## ENGINEERING EXPERIENCE
### Trimble, Inc. - Control Systems Software Engineer (Jan 2021 - Present)
- Developing control systems in the Trimble Autonomous Solutions division for agriculture and construction vehicles.

#### 2021 / 2022 
General responsibilities
- Developing Simulink models with custom embedded coder target for code generation in C.
- Co-authored the division’s simulink framework, used to deploy vehicle control systems to various hardware (ECU, embedded Linux)
- Established Simulink model style guidelines based off the Mathworks Advisory Board recommendations
- Design of autonomous vehicle control functions (steering, speed, vibration, obstacle detection) in Matlab/Simulink/Stateflow with unit tests
- Deeply familiar with Matlab Embedded Coder - including generating and building code for an vehicle  electronic control units (ECUs) using template make files, tlc files
- Experience wrapping C source code in an Simulink S-function
- Managed an RTOS to schedule tasks and manage controller CAN bus with vehicle
- Experience debugging ECU (lauterbach / TRACE32)
- Recorded manufacturer CAN schema in the form of a DBC file for use in encoding and decoding.
- Setup control system hardware in the loop (HIL) running with vehicle simulator. 
- Utilized ECU vendor API to configure EEPROM, intercore communication, CAN hardware
- Familiar with CAN J1939 concepts - address claiming, source/destination, broadcast, BAM
- Exposure to offroad safety standards for agriculture and construction and working on safety hardware

Outreach, leadership, and culture 
- Involved in student outreach, mentorship of intern program, sponsorship and advisement of local senior capstone projects
- 2022 Dimensions tradeshow - operated the offsite demonstration of a remote control bull dozer equipped with grade control
- Active presentor of lunch and learn knowledge sharing for Simulink development workflow and Mathworks toolboxes for functional safety.
- Lead quarterly hackathon teams to success resulting in the establishment of the main controls team source code repository
- Weekly feedback sessions with the ECU vendor to develop their Simulink SDK

#### 2023
Core responsibilities
- Built up the core controller libraries used in the autonomy systems
- Deployed control algorithms as debian packages
- Deprecated the legacy ECU and established the replacement embedded linux device as the core autonomy controller of the machine
- Developed CAN drivers for integrating with other Trimble products
- Controls lead for navgigating in a GNSS denied environment - led project planning and managed Jira project, roadmap, and deliverables to project team.
- Compiled evaluation of control system using odometry estimate into formalized report for project stakeholders
- Evaluation of the open source Nav 2 ROS stack
- Developed ROS 2 control system
- Implemented pure pursuit algorithm for navigation
- Configured off the shelf ROS implementation of extended kalman filter to estimate odometry in a GNSS denied environment 
- Lead generation of ROS packages from monolith code repository for the Controls team
- Selected GNSS components for a ground truth system and configured our local base station for RTK corrections
- Established the process for Simulink code generation to C++ and distributing as debian package.
- Ported algorithms for geofence and obstacle stopping to C++, generated wrappers for the implementation, and integrated into a ROS node.
- full software development lifecycle (design, development, test, deploy, integrate, hand-off)
- Implemented quality gates for core repository with requirements on formatting, static analysis, documentation, and unit tests.
- Identified options for technical documentation in repository (latex, PlanUML, markdown)
- Maintained technical documentation for onboarding new employees and getting development environment
- Familiar with using docker as a deployment mechanism on embedded linux
- Contributed a ROS REP-103 compliant version of our GNSS driver to the inner-source repository


Outreach, leadership, and culture
- Panelist for local university students regarding autonomous systems and career development
- Promoted Collaboration and re-use of internal autonomy components and libraries(inner-source) such as trajectory planner, GNSS drivers, ROS nodes, etc.
- Established team agile processes (Retrospective, standup, backlog grooming)
- Managed release process for core controller library (git tag, changelog, deployment to test/staging/production)


### Siemens Gamesa Renewable Energy, Engineering Project Support - Blade Inspection Camera May 2019 – Dec 2020
- Aided in commercializing a tower mounted turbine blade inspection device by developing a functional prototype
- Enhanced the concept of operation and created business case to market viability of the remote inspection method
- Improved inspection image accuracy of wind turbine blades using OpenCV to detect and track blade location
- Created command line interface to initiate inspection, debug log, image archive, and create spatial metadata

### Electro-Mechanical Products, Manufacturing Intern - Coherent Pressure Test Unit May 2018 – Aug 2018
- Developed an automated quality control unit to determine faulty heat exchangers and increase efficiency by 30%
- Implemented solenoid valves to automate wash, rinse, and dry cycle actuation using MOSFETs
- Amplified signals from a differential pressure transducer and thermocouple probe to be read by microcontroller
- Programmed microcontroller using Arduino IDE to display outputs, open valves, toggle relays, and read signals

## RELEVANT PROJECTS
### Police Academy Autonomous Vehicle, University of Colorado – Mechatronics and Robotics Jan 2020 – May 2020
- Collaborated in a team to deploy an autonomous robot capable of firing Nerf projectiles at targets
- Integrated packages for Ubuntu 18.04 on a Raspberry Pi including ROS, TensorFlow, and OpenVINO toolkit
- Implemented a proportional feedback loop with IR proximity sensors measurements to maneuver robot
- Developed machine learning model for target recognition and implemented on Intel Myriad X chip

### Control Systems Laboratory, University of Colorado Boulder – Quanser Experiments Jan 2020 – May 2020
- Developed an understanding of the full design process to introduce control laws for unknown systems
- Determined models of Quanser hardware modules using classical and Lagrangian mechanics
- Utilized frequency and time-based methods of system identification to determine model parameters
- Designed and incorporated classical control laws in Simulink for state space and transfer function representations
- Gained an intuition for tuning PID, LQR, and LQI controllers to meet performance specifications
- Experimented with state estimation using a derivative filter to perform state feedback on a ball and beam system

### Animal Care Systems, Senior Design Project (Test Engineer) - Mechanized Cage Monitoring Kit Aug 2018 – May 2019
- Designed a remotely accessible monitoring system for overnight viewing of laboratory setting
- Automated smooth rotation of carousel with stepper motor micro-stepping and rotational tracking via encoder
- Created GUI for remote control of motor and IR cameras utilizing an Apache server hosted on Raspberry Pi
- Developed and executed test procedures to verify vibration, noise, and light requirements for animal comfort

Independent Study, University of Colorado Boulder - Optimized Game Automation with GPU Jan 2019 – May 2019
- Designed a computer vision algorithm to detect tile position and estimate tile velocity for the game “Piano Tiles”
- Automated solenoid actuation based on visual servoing to emulate physical interaction with touchscreen
- Utilized accelerated parallel processing on a GPU with CUDA C/C++ to process frames from MIPI camera
- Increased computational efficiency such that the automated system exceeds the average human response time

## SOFTWARE/TECHNICAL SKILLS
- Proficient in C/C++, Python, Bash, MATLAB, Simulink, Dart
- Frameworks: CUDA, OpenCV, ROS, Google Test, Flutter, Gazebo
- Design: SolidWorks, Fusion 360, 3D printing (Cura, Prusa), PlantUML, Lucidchart
- Development environment: Linux, VS Code, Github Copilot, clang
- Tools: Microsoft Office, Google Suite, Docker, CMake, git, Bitbucket, Github, Jira, Confluence, Bamboo, Doxygen, Foxglove, Plot Juggler
- Quality Assurance: cppcheck, clang-tidy, clang-format
- Hardware experience with Raspberry Pi, NVIDIA Jetson Nano, Arduino, National Instruments, Quanser, Embedded Linux
- Sensors: Camera, Radar, CAN enabled devices
- Communication protocols: Serial, CAN, TCP/IP (Primarily UDP)
- Technologies: GNSS (RTK + RTX)