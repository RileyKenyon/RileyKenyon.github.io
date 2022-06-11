---
name: Automated Quality Control Unit
tools: [C, microcontroller, integration]
image: /img/2019/EMP_box2_ptest.jpeg
description: Re-designed a manual pressure test unit to create an automated solution. The micro-controller powering the logic of the device is a Itsy Bitsy. The peripherals of the unit include a differential pressure transducer, thermo-couple, pump, heater, fan, solenoid valves, flow sensor, and more. 
---
# Coherent Pressure Test Unit 

**Company**: Electro-Mechanical Products (EMP)

**Project**: Coherent Pressure Test Unit

**Role**: Manufacturing Intern

The coherent pressure test unit was a test apparatus used to determine if flux or solder from manufacturing heat exchangers was influencing fluid flow (thereby creating a localized hot spot). The original design consisted of 7 valves manually operated to control various processes needed to clean the part and test the flow. See the image below for reference.

![alt text](/img/2019/EMP_01.jpg "Original Quality Control Unit")

The first step in preparing the heat exchanger was to flush the tubing with water, to rid any preliminary debris/solder. The secondary process was to send an alconox detergent solution through to neutralize and clean the internals of any flux. Afterwards, the heat exchanger is flushed with water and the pressure differential is measured to determine the pressure drop from between the inlet and outlet. Lastly the tubing is flushed with air and removed from the test-stand. 

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/362684976" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

In order to automate the process and allow for more productive time (manually switching between process steps occurred approximately every 5 minutes), I designed a new pressure test unit using a micro-controller (Itsy-Bitsy), solenoid valves, and several peripherals.

{% capture carousel_images %}
/img/2019/EMP_box2_ptest.jpeg
/img/2019/EMP_02.jpg
/img/2019/EMP_03.jpg
/img/2019/EMP_04.jpg
/img/2019/EMP_05.jpg
/img/2019/EMP_06.jpg
/img/2019/EMP_07.jpg
/img/2019/EMP_arduino-layoutv2.png
{% endcapture %}
{% include elements/carousel-custom.html %}


The deliverables and skills learned from the project are summarized as:

* Designing and implementing an semi-automated solution to increase productivity while reducing the cost of a unit
* Reading datasheets and designing electrical circuits for use in amplifying signals and actuating peripherals using MOSFETs
* Creating rapid prototypes and testing proofs of concept
* Exposure to a manufacturing facility – and the type of quality control needed to ensure reliability

This internship and opportunity sparked my interest in signals and systems – influencing my career aspirations and providing experience with sensor integration. The outcome of the project was an increased efficiency in water usage while automating the system cycle – thereby freeing up the time of a technician. 


