# Gumstix-Self-Driving-Car
## Project Description
This project is a embededd system course project. The aim of this project is to detect Stop-sign & Yield signs for autonomous motion of the car, which is based on Gumstix board. Using linux’s inbuilt device drivers, we obtain the image frames, convert them to RGB values, and do thresholding on these pixels to detect red or blue colours. A kernel module on gumstix, then uses flags to determine which GPIO pins to be enabled, and move the car in forward/stop or reverse direction.
## Project Component
