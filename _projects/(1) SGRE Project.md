---
name: Siemens Gamesa Renewable Energy - Tower Mounted Camera
tools: [openCV, python, R&D]
image: /img/2019/SGRE_tower.jpg
description: Aided in the implementation of a novel solution for external blade inspections. Developed a smart-recognition script using OpenCV to aid in automation. 
---
# Automated Blade Inspection Camera

**Project** : Automated Blade Inspection Camera

**Role**: Engineering Project Support 

{% include elements/figure.html image="/img/2019/turbinetop.jpg" caption="Riley Kenyon standing on top of a SWT-2.3 108 in Golden, CO."%}

The novel solution for external wind turbine blade inspections is proprietary and undergoing patent approval. Starting as a tech-scouting (senior design) project through the University of Colorado Boulder, the Service R&D team at Siemens Gamesa Renewable Energy (SGRE) decided to move forward with developing the design further. I was brought on to the company during May 2019 to aid in the further development. 

My main responsibilities include:
* Making amendments to the design to implement a functional prototype
* Using computer vision to create “smart recognition” scripts that provide feedback related to the inspection process
* Developing associated documentation to move the project forward as a product (business case, technical requirement specification), and interfacing with entities (external and internal) such as SCADA, cyber-security, product lifecycle management to ensure compliance





The day-to-day work varies between testing functionality at the Boulder test site (NREL Flatirons Campus, formerly National Wind Technology Center (NWTC)), working remotely on development, and working at the office to create documentation.

{% capture carousel_images %}
/img/2019/SGRE_tower.jpg
/img/2019/SGRE_tip_hsv.png
/img/2019/SGRE_cv_center.jpg
{% endcapture %}
{% include elements/carousel-custom.html %}

The skills learned from the project are summarized as:

* Experience writing Python scripts – specifically making use of pywheels, creating modules and classes, and getting packages through pip
* Experience using numpy and openCV libraries in python for computer vision and object detection (histogram peak detection, colorspaces, segmentation, edge detection, features, center area moments, etc.)
* Serial communication with a set of servo motors to control location of camera within enclosure (allowing the camera to pan/tilt through the whole blade)
* Linux (Ubuntu, Raspbian) familiarization with cross-platform development
* Familiarity with source code revision control through git 
* Creating a command line interface to specify input values for inspection, while being modular for expansion
* Exposure to wind renewable energy, familiarity with turbine components, blade defects and composition

{% include elements/figure.html image="/img/2019/SGRE_testturbine_a_pressureside-1.png" caption="Stitched image of pressure side of Boulder Turbine T-01 utilizing meta-data and images acquired from the automated blade inspection camera." %}

This position gave me an opportunity to implement computer vision on a SOC utilizing python while simultaneously exposing me to how business and product development operates within a large company.
