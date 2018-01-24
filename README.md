# Gumstix-Self-Driving-Car
## Project Description
This project is a embededd system course project. The aim of this project is to detect Stop-sign & Yield signs for autonomous motion of the car, which is based on Gumstix board. Using linux’s inbuilt device drivers, we obtain the image frames, convert them to RGB values, and do thresholding on these pixels to detect red or blue colours. A kernel module on gumstix, then uses flags to determine which GPIO pins to be enabled, and move the car in forward/stop or reverse direction.
## Project Components
* Camera: Logitech Y270 Webcam
* Motor driver: L293D
* Self made mobile car: moter power supply 3V - 6V
* Battery: for moter driver: 9V battery stepped down to 5V using a regulator; for Gumstix: 5V, 1A
## How to run
1. Go to Gumstix kernel
2. Insert the camera modules following these steps:
* insmod v4l2-common.ko
* insmod v4l1-compat.ko
* insmod compat_ioctl32.ko
* insmod videodev.ko
* insmod uvcvideo.ko
3. Unzip km.zip file and go to this folder, and do these steps:
* make clean
* make
4. Transfer motor.ko to gumstix
5. run the command to initialise the device file:
* mknod /dev/motor c 61 0 
