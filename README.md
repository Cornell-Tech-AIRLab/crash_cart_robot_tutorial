# CRASH-CART-ROBOT-TUTORIAL-HRI 🤖

Crash Cart Robot Tutorial 

<p align="center"> 
<img src="./images/airlablogo.png" width="50%"> 

This tutorial provides step-by-step instructions to build a low-cost cart robot with multimodal feedback capabilities using speech, drawer lights, and alerts to indicate the location of relevant supplies and task reminders.

See the Tutorial on [YouTube](https://www.youtube.com/watch?v=EV-0HwNPJiY).

Taylor, A., Tanjim, T., Sack, M., Hirsch, M., Cheng, K., Ching, K., St. George, J., Roumen, T., Jung, M., Lee, H. (2025) “Rapidly Built Medical Crash Cart! Lessons Learned and Impacts on High-Stakes Team Collaboration in the Emergency Room.” In Proc. of the 20th Annual ACM/IEEE Conference on Human Robot Interaction (HRI).

<p align="center"> 
<img src="./images/crash_cart_setup.png" width="50%"> 
<i>

<b>Figure 1:</b> We built a series of teleoperated medical crash cart robots. Prototype 1 delivers supplies using a hoverboard circuit. Prototype 2 also delivers supplies, recommends supplies using drawer opening capabilities, and was deployed at a medical training event which revealed insights which led to the design of Prototype 3 that communicates recommendations and reminders using drawer lights, speech, and alerts.

</i> 
</p>

## System Requirements
- Ubuntu Version???
- Python Version???
- Robot Operating System 2 (Distribution ???)

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

1.1 Download the version of the Raspberry Pi Imager application compatible with your computer https://www.raspberrypi.com/software/.

1.2 Insert the micro SD card into your computer directly or through an adapter.

1.3 Open the Imager and fill out the following options:

1.4 Raspberry Pi Device: Raspberry Pi 4
- Operating System: Other general-purpose OS → Ubuntu → UBUNTU DESKTOP 22.04.4 LTS (64-BIT)
- Storage: Your SD Card reader


<p align="center"> 
<img src="./images/figure1.png" width="50%"> 
<i>

<b>Figure 1:</b> Set up a micro-SD card for Raspberry PI 4 using Imager application.
</i> 
</p>

1.5 Click “NEXT” and wait around eight minutes for the imager to write successfully.

1.6 Once complete, safely remove the card. 

1.7 Insert the microSD card into the Raspberry Pi with its metal bits facing the bottom of the Pi.

### Step 2: Attach the LED strip to the cart (10 minutes)

2.1 Peel some of the adhesive back off of the LED strip and start attaching it to the cart. If the adhesive isn’t strong enough, you may need glue or tape.

2.2 Make sure around two LEDs correspond nicely to each drawer to make it easier for the cart to give clear instructions regarding which drawer a user should select.

If struggling to align the LEDs with the drawers, gently pinch the LEDs as shown below to adjust their positions.

<p align="center"> 
<img src="./images/figure2.png" width="50%"> 
<i>

<b>Figure 2:</b> Attach LED lights to the cart.
</i> 
</p>

2.3 Once attached to one side, curve the strip under the cart, run it along the bottom, and have it curve up to the other side.

2.4 When attaching the strip to the other side, make sure to keep the lighting symmetrical. Mirror the positioning of each individual LED to ensure level lighting across the cart. It should look like this:

<p align="center"> 
<img src="./images/figure3.png" width="50%"> 
<i>

<b>Figure 3:</b> LED lights installed to ensure uniform lighting across the cart.
</i> 
</p>

2.5 Once you’ve lined up the LEDs, cut the excess on the white line with the copper strips.

### Step 3: Connect Electronics (10 minutes)

3.1 Make sure you put in the Micro SD card before you plug the Pi into the outlet!

<b>General wiring</b>

3.2 Connect your monitor to the outlet using the female/male plug cable.

3.3 Connect your Raspberry Pi to the outlet using the mini USB/male plug cable.

3.4 Connect your monitor to the Raspberry Pi using either your HDMI/micro HDMI cable or VGA/micro HDMI cable, depending on which port your monitor contains.

3.5 Connect your keyboard to the Raspberry Pi using its wire to USB A.

3.6 Connect your mouse to the Raspberry Pi using its wire to USB A.

3.7 For the jumper wires:
- Connect the red wire to a 5V power pin (Pin #2 or #4 on a Pi 4)
- Connect the black wire to a ground pin (Pin #6 on a Pi 4)
- Connect the green wire to the GPIO 18 pin (Pin #12 on a Pi 4)

<p align="center"> 
<img src="./images/figure4.png" width="50%"> 
<i>

<b>Figure 4:</b> Electronic wiring connections for Raspberry Pi 4 with monitor, keyboard, mouse, and LED using appropriate wires and ports.
</i> 
</p>

### Step 4: Boot the Raspberry Pi (12 minutes)

4.1 Once the monitor is connected to the RPi4 to a power outlet, make sure its input is switched to either VGA or HDMI, depending on the port you connected the Pi to.

4.2 The Pi should boot with a rainbow screen, then a black one with some white text in the top left corner, and then the Ubuntu loading screen. It should then open to a really cute jellyfish background.

4.3 Wait a second, then the screen should start to ask you about your settings.

4.4 Enter your desired settings, and make sure to connect to wifi now to save time later.

4.5 Submit your choices, then wait for the system to configure. This may take some time.

4.6 The computer should then reboot, allowing you to sign in.

4.7 When it opens, system program problems and internal errors may pop up, you can ignore those messages.

4.8 You can skip through the setup instructions, and once you’re done, congratulations! You’ve set up an Ubuntu operating system on a Raspberry Pi.

### Step 5: Download necessary files (6 minutes)

5.1 Open a web browser (such as Firefox) to access the project GitHub repository on your monitor: https://github.com/Cornell-Tech-AIRLab/crash_cart_robot_tutorial

5.2 Press the green “Code” dropdown button.

<p align="center"> 
<img src="./images/figure5.png" width="50%"> 
<i>

<b>Figure 5:</b> Downloading necessary files from the Github repository.
</i> 
</p>

5.3 Click the “Download ZIP” button and wait for it to download.

5.4 Open the zip files, then right-click the file and press “Extract Here.”

<p align="center"> 
<img src="./images/figure6.png" width="50%"> 
<i>

<b>Figure 6:</b> File extraction of the GitHub Repository.
</i> 
</p>

5.5 Open the resulting folder and right-click the robot_communication_ws zip file and press “Extract Here.”

5.6 Make sure to wait for the extracted successfully popup, as not doing so will cause future issues. Then, drag the “robot_communication_ws” folder along with the “ros2_installation.bash” and “tool_installation.bash” files to “Home.”

5.7 Double-check check that everything was moved properly to the ‘Home’ folder.

<p align="center"> 
<img src="./images/figure7.png" width="50%"> 
<i>

<b>Figure 7:</b> Bash file setup.
</i> 
</p>

### Step 6: Download Robot Operating System 2 (55 min)

6.1 Go to the bottom left of your screen and view your applications.

6.2 Click “Terminal” to open a terminal window.

6.3 Right-click the Terminal icon on the left side menu and click “Add to favorites” for easy access in the future.

6.4 Type in the following command and press enter: 
```
bash ros2_installation.bash
```

This will install Robot Operating System 2, or ROS2. This will let us easily control the robot

6.6 Then enter your monitor’s password. Your keyboard is typing, even though characters won’t appear.

6.7 Let the program run. Use the next 50 minutes of loading time to watch cars pass by, contemplate existence, or take a nap.

6.8 Make sure to check the screen every so often, though, as it will ask you to press enter or enter a capital Y for permissions a few times.

6.9 Once it finishes running, it’s time to test the fruits of your hard work! Open two new terminal windows and close the old one.

6.10 Enter the following commands in the terminal:
```
source /opt/ros/humble/setup.bash
ros2 run demo_nodes_cpp talker
```

6.11 Then enter these into another terminal:
```
source /opt/ros/humble/setup.bash
ros2 run demo_nodes_py listener
```

6.12 If the first window is saying that it's publishing ‘Hello World’ and the second says it’s hearing ‘Hello worlds, yippee!’ You’ve installed ROS2 successfully :)

If not, try googling your error message to debug.

### Step 7: Install necessary tools (6 min)

7.1 Open a new terminal window and enter the following. This will install the tools necessary for the program to run properly. Wait around six minutes for it to finish running:
```
bash tool_installation.bash
```

### Step 8: Test and edit light code for compatibility (25 minutes)

8.1 Open a new terminal window and run the following to run the light node
```
source /opt/ros/humble/setup.bash
colcon build --symlink-install
cd robot_communication_ws
source install/setup.bash
ros2 run light_pkg light_node
```

8.2 Try pressing a couple of the buttons and watch the lights on the carts flash. You may have noticed that the buttons don’t light the correct LEDs. If this is the case, you must edit the code to be compatible with your cart.

8.3 Go to your files, follow this file path, and open the py file: Home → robot_communication_ws → source → light_pkg → light_pkg → light_node.py

8.4 Open a new terminal window and rerun the module by entering the following (quick tip, if you press the up arrow you can the following commands in your history and can enter them like that to make it easier):
```
source /opt/ros/humble/setup.bash
colcon build --symlink-install
cd robot_communication_ws
source install/setup.bash
ros2 run light_pkg light_node
```

8.5 Once you’ve run the program, click the first button and watch to see which lights flash. If only one pair lights up, the program is trying to light LEDs we’ve cut off.

8.6 Go to the portion of the light_node code shown below. 

<p align="center"> 
<img src="./images/figure8.png" width="50%"> 
<i>

<b>Figure 8:</b> Code snippet for modifying RGB values, LED colors, and corresponding LED lights. 
</i> 
</p>

8.7 Each four-line section of code corresponds to one button on the pop-up, one drawer that needs to be lit. Editing the number in the square brackets for the first section will change which LED is lit when the first button is pressed. Increasing the number will make the lit LED further from the end with the wires, decreasing it will make the LED closer to that end.

8.8 Edit the number, press the save button at the top of the code’s window, press Control C in the terminal window to stop the program, open a new window, then rerun the node:
```
source /opt/ros/humble/setup.bash
cd robot_communication_ws
source install/setup.bash
ros2 run light_pkg light_node
```

8.9 Look to see which LEDs light up now. Is it still too far one way? Or maybe now too far the other way? Repeat step h until each button properly lights a different drawer from both sides with the final two buttons flashing all the lights. This should take around 15 minutes.

<p align="center"> 
<img src="./images/figure9.png" width="50%"> 
<i>

<b>Figure 9:</b> LED lights installed across the mobile crash cart.
</i> 
</p>

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

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

Fork the repo and create a pull request to improve the tutorial. You can also simply open an issue with the tag "enhancement". Don't forget to give the project a star! Thanks again!
- Fork the Project
- Create your Feature Branch (git checkout -b feature/AmazingFeature)
- Commit your Changes (git commit -m 'Add some AmazingFeature')
- Push to the Branch (git push origin feature/AmazingFeature)
- Open a Pull Request


## Further Issues and questions ❓ 

If you have issues or questions, don't hesitate to contact:

Anaiya Z. Badi (anaiya.badi@gmail.com)
Tauhid Tanjim (tt485@cornell.edu)
Angelique M. Taylor (amt@cornell.edu)