# keil-driver-uart
One of my repositories for the 'Embedded Systems Object-Oriented Programming in C' course. 

## keil isntallation and bug

To download the keil IDE, just click [here](https://www.keil.com/demo/eval/arm.htm#!#DOWNLOAD).

Sadly I lost a lot of time trying to make the uVision Keil 5 find the installed packs of STM32. The issue and solution for my problem is similary to [this topic](https://community.arm.com/support-forums/f/keil-forum/46602/can-t-find-any-device-after-installing-the-package) in the ARM community. With all packs previous installed I just re-install the IDE and then it worked.

## Creating a new project and configurating the environment to build and debug the project

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

![image](https://user-images.githubusercontent.com/58916022/211565028-257ae3eb-cd53-4127-957a-43798c12b924.png)

7. Change the ARM compiler from 'C 90' to 'C99' to fix the conflict of Device Family Pack requirement.

![image](https://user-images.githubusercontent.com/58916022/211565205-214826f9-7be1-4f5c-868d-bdb467e63df3.png)

7.a Click in the 'Options for target' icon. On the 'C/C++ (AC6)' tab change in 'Language / Code Generation' -> 'Language C' the 'c90' option to 'c99'. Then click 'OK'. 

![image](https://user-images.githubusercontent.com/58916022/211566575-f4aedb34-bbd4-40d7-bad0-e4ccaf7210ce.png)

7.b The instructor asks to change to 'ARM Compiler:' -> 'Compiler Verion 5'. But since it's missing.

![image](https://user-images.githubusercontent.com/58916022/211566231-3fcd4948-1fe5-4e9f-9fbc-d21b46d2f274.png)

NOTE: When compiling the code, errors appeared refering the stdio lib, then we will install the 'Compiler Verion 5'. But always when creating a new project, the last version is recommended.

![image](https://user-images.githubusercontent.com/58916022/211583978-24bde721-dcb8-44c8-9b2a-fd6a2c0d831b.png)

7.b To add missing compiler I followed [this article](https://developer.arm.com/documentation/ka005073/latest#:~:text=While%20Arm%20Compiler%205%20is,Existing%20projects.) from developer.arm website.

To download the 'Compiler Verion 5' you must login to ARM website. And sadly, after creating an account to do that, the following message appear:

![image](https://user-images.githubusercontent.com/58916022/211583153-9b367a6d-ff10-41b7-bcc4-094dcfa788af.png)

Then I was getting error when trying to download the compiler:

![image](https://user-images.githubusercontent.com/58916022/211800401-068da728-3da1-4edf-978e-097debd891b8.png)

I Contacted ARM team and they asked me to try a different browser. Tried again and it worked! After download I just unziped and isntalled (.exe file).

![image](https://user-images.githubusercontent.com/58916022/211800664-da61f066-1aed-4a01-9383-acce47932155.png)

Then I wen to 'Project' -> 'Manage' -> 'Project Items...'

![image](https://user-images.githubusercontent.com/58916022/211802154-73a93494-a52b-4c6e-b132-0c686b381b09.png)

Then in 'Folder/Estensions' tab I clicked on ellipsis buttom.

![image](https://user-images.githubusercontent.com/58916022/211802642-b12e1a6e-bb97-44bb-b7be-8fbb0c37c970.png)

And then 'Add another ARM Compiler Version to List...'.

![image](https://user-images.githubusercontent.com/58916022/211802894-15b80b21-f41c-44dd-a4b8-bfea30a8c49c.png)



#### 8. To build project click at 'Build' icon.

![image](https://user-images.githubusercontent.com/58916022/211577685-637ebed5-35ad-4d38-aa65-6c90443e6d66.png)

9. To select debugger, go to 'Options for Target...' icon.

9.a Then in the 'Debug' tab, select the 'ST-Link Debugger'.

![image](https://user-images.githubusercontent.com/58916022/211578721-6cb2f361-0552-4d3d-9d5d-333e0848c224.png)

9.b Then click in 'Settings' and in the 'Flash Download' tab, in 'Download Function' tick the option 'Reset and Run'. Then click in the 'OK' button and 'OK' again.

![image](https://user-images.githubusercontent.com/58916022/211579721-dfd13550-6fc2-47b4-96bf-841cc70c616e.png)

10. To send to the board click at 'Download' icon.

![image](https://user-images.githubusercontent.com/58916022/211577906-92e4f7ba-4b0c-4367-aaf0-32a877977f2c.png)

## codes

