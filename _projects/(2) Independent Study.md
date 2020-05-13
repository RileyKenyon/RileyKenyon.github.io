---
name: Optimized Game Automation with GPU
tools: [GPU, C, Cuda]
image: /img/2019/IndStudy_best-rotated.jpg
description: Implemented visual servoing using computer vision and GPU accelerated processing for phone game 'Piano Tiles'
---

# Independent Study
This project was an Independent Study performed with Dr. Shalom Ruben to utilize a GPU for visual servoing. At the time of the project development, Nvidia had just released the Jetson Nano – a SOM (system on module) for affordable computer vision, deep learning, etc. The more expensive system (Jetson TX2) was used initially for setup and preliminary testing of GPIO and CUDA programming. The two systems were used to develop the code, but ultimately the implementation finished on the Nano. 

The goal of the project was to use frames from a Raspberry Pi camera to determine when to tap the phone screen while playing the game “Piano Tiles”. A previous attempt was made using a Raspberry Pi, but the result was a failure at 7 in/s (the speed of the screen). Although fast, a human could still tap faster and beat the machine. See the improvements on the GPU with a record of 11 in/s. 
The final report of the project can be found here.
{% include elements/button.html link="/img/2019/finalreport_rileykenyon_sp2019-1.pdf" text="Report" %}

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/362217850" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
