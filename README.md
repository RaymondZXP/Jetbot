# Jetbot Documentation for Micron Robotic Event Day 


Welcome, Micron AGV interns!

This repository contains the modified notebooks for the Micron Robotic Event Day, created by the 2019/20 semester 2 batch of micron AGV interns.


## Hardware Setup

For the hardware installation, please follow the original link provided by the waveshare jetbot documentation www.waveshare.com/wiki/JetBot_AI_Kit. 

### IMPORTANT 

1. Please flash the Jetbots with Jetbot Image v3.2. This repository is ONLY compatible with jetbot image version 3.2. Jetbot image version 3.2 is built with TensorRT 5.0 while Jetbot image version 4 is built with TensorRT version 6.1. 
  
  ```
   from jetbot import ObjectDetector 
  ```

  in the ```object_following``` folder, ```Object Following Tutorial.ipynb``` only works with TensorRT version 5.0. 

2. In Step 6. Configure power mode of the waveshare jetbot documentation, in addition to the command

```
sudo nvpmodel -m1
```

  Please run 
  
  ```
  sudo nvpmodel -m0
  ```
  
  followed by 
  
  ```
  sudo nvpmodel -m1
  ``` 
  again
  
  This is to reset the power mode of the PCB to the default status before setting it to 5W mode. We have found out this step is very crucial for the hardware installation. 
  


## Package Content
There are 5 folders in total:

1. The first two folders ```basic_motion``` and ```teleoperation``` contains mostly original notebook from the waveshare Jetbot documenation. You can get familiar with the basic operation of the jetbot with this two files. Alternatively, clone the original repository from the waveshare website to see the unmodified notebooks.

2. The ```collision_avoidance```, ```object_following``` and ```sign_detection``` folders contains the modified notebooks inserted with comments. Do refer to the comments for important notes. The link to the trained models are given in the Readme file under the respective folder

### Some Known Issues

1. There are issues with the camera of the Jetbot. Creating a new ```Camera.instance()``` in one notebook will prevent other notebooks from creating a new camera instance. Also, it is important to shutdown the camera instance with ```camera.stop()``` before creating a new camera instance. If the camera instance is not properly terminated, the only solution we have found out is to reboot the Jetbot.Therefore, please be graceful with the Camera!!!

2. Please pay constant attention to the status of the jupyter notebook. It is supposed to be ```idle``` when you are not running anything and ```busy``` when you are running some codes. ```unknown``` status indicates that there might be internet connection problems with the jupyter notebook (which happens a lot!). You may want to consider reconnecting after waiting for a while.

3. There is significant inconsistency between the qulities of the motors and PCBs, therefore parameters such as speed and turn_gain need to be tuned for each jetbot. Just do some trial and error to find the acceptable speed.

4. As you may have noticed, there is no indication for the battery level of the Jetbot. Therefore, its is recommended to always charge the jetbot while you are prgramming it and only disconnect the charger when you are testing it on the ground. It is important to let the participants to note this during the event!

Good Luck and Have Fun!
