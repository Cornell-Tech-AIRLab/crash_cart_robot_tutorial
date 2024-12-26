# CRASH-CART-ROBOT-TUTORIAL-HRI 🤖

Crash Cart Robot Tutorial 

This tutorial provides step-by-step instructions to build a low-cost cart robot with multimodal feedback capabilities using speech, drawer lights, and alerts to indicate the location of relevant supplies and task reminders.

See the Tutorial on [YouTube](https://www.youtube.com/watch?v=EV-0HwNPJiY).

Taylor, A., Tanjim, T., Sack, M., Hirsch, M., Cheng, K., Ching, K., St. George, J., Roumen, T., Jung, M., Lee, H. (2025) “Rapidly Built Medical Crash Cart! Lessons Learned and Impacts on High-Stakes Team Collaboration in the Emergency Room.” In Proc. of the 20th Annual ACM/IEEE Conference on Human Robot Interaction (HRI).

<p align="center"> 
<img src="./images/crash_cart_setup.png" width="50%"> 
<i>

<b>Figure 1:</b> We built a series of teleoperated medical crash cart robots. Prototype 1 delivers supplies using a hoverboard circuit. Prototype 2 also delivers supplies, recommends supplies using drawer opening capabilities, and was deployed at a medical training event which revealed insights which led to the design of Prototype 3 that communicates recommendations and reminders using drawer lights, speech, and alerts.

</i> 
</p>

Contents: 
- [Introduction](#introduction) 
- [Materials and Supplies](#materials_supplies) 
- [Medical Crash Cart Robot Tutorial Steps](#medical_crash_cart_robot_tutorial_steps) 

## Introduction

Designing robots to support high-stakes teamwork in emergency settings presents unique challenges, including seamless integration into fast-paced environments, facilitating effective communication among team members, and adapting to rapidly changing situations. While tele-operated robots have been successfully used in high-stakes domains such as firefighting and space exploration, autonomous robots that aid high-stakes teamwork remain underexplored. To address this gap, we conducted a rapid prototyping process to develop a series of seemingly autonomous robot designed to assist clinical teams in the Emergency Room. We transformed a standard crash cart—which stores medical equipment and emergency supplies into a medical robotic crash cart (MCCR). The MCCR was valuated through field deployments to assess its impact on team workload and usability, identified taxonomies of failure, and refined the MCCR in collaboration with healthcare professionals. Our work advances the understanding of robot design for high-stakes, time-sensitive settings, providing insights into useful MCCR capabilities and considerations for effective human-robot collaboration. By publicly disseminating our MCCR tutorial, we hope to encourage HRI researchers to explore the design of robots for high-stakes teamwork.

You can use this bibtex to cite this work ([Taylor et al.](https://www.angeliquemtaylor.com/), 2025): 

``` 
@article{taylor_2025, 
author = {Taylor, A., Tanjim, T., Sack, M., Hirsch, M., Cheng, K., Ching, K., St. George, J., Roumen, T., Jung, M., Lee, H.}, 
title = {Rapidly Built Medical Crash Cart! Lessons Learned and Impacts on High-Stakes Team Collaboration in the Emergency Room.}, 
journal = {In Proc. of the ACM/IEEE Conference on Human Robot Interaction (HRI).}, 
year = {2025}
}
```

## Materials and Supplies

## Medical Crash Cart Robot Tutorial Steps

### Step 1: Set up micro SD card (12 minutes)
### Step 2: Attach the LED strip to the cart (10 minutes)
### Step 3: Connect Electronics (10 minutes)
### Step 4: Boot the Raspberry Pi (12 minutes)
### Step 5: Download necessary files (6 minutes)
### Step 6: Download Robot Operating System 2 (55 min)
### Step 7: Install necessary tools (6 min)
### Step 8: Test and edit light code for compatibility (25 minutes)
### Step 9: Connect the Bluetooth speaker (1 minute)

9.1 Make sure your speaker is turned on and in range.

9.2 Go to the top right corner of the screen. Click “Bluetooth On”, then “Bluetooth Settings”. Once your speaker pops up, click its name and switch on the connection.

### Step 10: Test the alert module (1 minute)

10.1  Open a terminal and run the following commands to test the alert module:
```
cd robot_communication_ws
source install/setup.bash
ros2 run alert_pkg alert_node
```

10.2 Click the buttons, and you should hear beeping!

### Step 11: Test the dialogue module (1 minute)

11.1 Open a terminal and run the following commands to test the dialogue module:
```
cd robot_communication_ws
source install/setup.bash
ros2 run dialogue_pkg dialogue_node
```

11.2 Click the buttons, and you should hear the robot’s dialogue.

## Congratulations! You are now the proud owner of a robotic crash cart.

