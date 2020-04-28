
Please download the engine file before runnning the code.

The ``` ssd_mobilenet_v2_coco.engine ``` file can be downloaded from [here](https://drive.google.com/open?id=1lpKBOAuUMX7RdzhFDIPSxDRSWU3Lea2e)

The original Notebook tries to run the collision avoidance model and the object following model in parallel. We have found out that it is too heavy for the Jetson Nano and hence removed the collision avoidance part.

The ```speed``` and ```turn gain``` setting in the notebook may be different from Jetbot to Jetbot, due to the inconsistency in the quality of the motors and PCBs. Therefore please tune these parameters while runnning the code.
