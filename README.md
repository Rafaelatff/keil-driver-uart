# keil-driver-uart
One of my repositories for the 'Embedded Systems Object-Oriented Programming in C' course. 

## keil isntallation and bug

To download the keil IDE, just click [here](https://www.keil.com/demo/eval/arm.htm#!#DOWNLOAD).

Sadly I lost a lot of time trying to make the uVision Keil 5 find the installed packs of STM32. The issue and solution for my problem is similary to [this topic](https://community.arm.com/support-forums/f/keil-forum/46602/can-t-find-any-device-after-installing-the-package) in the ARM community. With all packs previous installed I just re-install the IDE and then it worked.

## Creating a new project

1. Go to 'Project' -> 'New uVision project...'

![image](https://user-images.githubusercontent.com/58916022/211558057-c5907b15-e202-4385-89cb-094671e47700.png)

2. Select the folder for the project and then click 'Save/Salvar'.

![image](https://user-images.githubusercontent.com/58916022/211558301-05466caa-7546-49cb-a5b0-99642879397b.png)

3. Select the device from manufacturer three and then click 'OK'.

![image](https://user-images.githubusercontent.com/58916022/211558525-584c9263-1e62-4d13-8ebd-69349f629031.png)

4. In the 'Manage Run-Time Environment' page select, under the software component 'CMSIS' -> 'CORE' and tick the option 'CMSIS-CORE for Cortex-M ..'. Then under 'Device' -> 'Startup' tick the 'System Startup for STMicroelectronics STM32F4 Series' option.

![image](https://user-images.githubusercontent.com/58916022/211559185-0606fffe-3026-463b-bcce-e527ed4f71b9.png)

5. In the project three, change the 'Target 1' folder name to the microcontroller family ('STM32F4'). The folder 'Source Group 1' change to 'App'.

![image](https://user-images.githubusercontent.com/58916022/211560224-37218104-8b35-419e-bba8-baf4c2c270cf.png)

6. Create 3 files inside the 'App' folder. Two source files named 'main.c' and 'uart.c' and a header file with the name 'uart.h'.
