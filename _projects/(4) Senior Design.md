---
name: Senior Design Project
tools: [arduino, python, integration, testing]
image: /img/2019/SD_final-expo-poster.png
description: Designed and integrated a motorized fixture to remotely rotate a 500 lb inertia through a GUI hosted on a Raspberry Pi. Implemented a live video feed to remotely monitor and fine-tune the system.
---
# Senior Design Project - University of Colorado, Boulder
**Project**: Animal Care Systems (Company), Mechanized Motor Kit

**Role**: Test Engineer

The mechanized motor kit is an add-on for Animal Care System’s Optimice 100 animal carousel – these units are used for monitoring mice in laboratory settings. In order to make it the most comfortable for the nocturnal animals, the desired monitoring scenario is overnight. Instead of sending a technician to perform observation, the add-on kit we developed could be used to remotely monitor the mice and rotate the chassis. The main learning goals over the project were:

* Client/Server side scripting for a server hosted on a Raspberry Pi for signal output through a web-interface
* Specifying components and integrating an electrical system to rotate the carousel (PSU, Bi-Polar stepper motor, stepper driver, controller)
* Understanding micro-stepping for stepper motors and the associated torque losses
* Noise and vibration testing

{% capture carousel_images %}
/img/2019/SD_animalcaresystems.jpg
/img/2019/SD_communicationschematicv6.png
/img/2019/SD_final-expo-poster.png
/img/2019/SD_gui_layout.png
/img/2019/SD_motor.jpg
/img/2019/SD_teamphoto.png
{% endcapture %}
{% include elements/carousel-custom.html %}

<div class="container-fluid">
 <div class="row">
    <div class="col-sm">
      <iframe src="https://player.vimeo.com/video/362662367" style="display: block; margin: auto;" height="640" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
    </div>
    <div class="col-sm">
      <iframe src="https://player.vimeo.com/video/362662352" style="display: block; margin: auto;" height="640" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

    </div>
</div>

For this project, students were assigned to teams of 6 to simulate working with other engineers on a project. Within our team, I elected to be the test engineer on the project. My duties included creating a test plan to satisfy all the design requirements and specifications. Additionally, I determined the hardware used in the design as well as the full integration of components. 
