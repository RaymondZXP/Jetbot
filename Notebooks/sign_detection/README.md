As commented in ```live_demo_sign_detection.ipynb```, we are using similar concepts of image classification.

The model we have trained can be downloaded [here](https://drive.google.com/open?id=1FYCPo4fLVlf1l_GMvk_ABhMpD4hhDEId)

Please note that for the purpose of the real Robotic Event Day, the you may need to re-collect image data on the event venue with your newly designed signs. This model is only trained based on image collected in the workstation with the follwing designs:

###### Stop Sign


###### Right Sign


###### Left Sign

and the other two classes ```free``` and ```blocked``` are trained on teh same dataset gathered in ```collision_avoidance``` folder.

Therefore the model may not work very well outside the workstation due to overfitting. 

Feel free to change the design of the sign or even the model for better performance!


