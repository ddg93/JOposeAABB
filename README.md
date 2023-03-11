# Welcome to the JOposeAABB repository 

This GitHub project provides a deep learning model for accurate pose estimation of cylinders and ellipsoids suspended in a viscous shear flow.

The model estimates the particle orientation vector from the experimental measurements of the three-dimensional Axes-Aligned Bounding Box (AABB) of the oriented axisymmetrical particle. 

![alt text](https://github.com/ddg93/JOposeAABB/blob/main/setup_complete.jpg?raw=true)

As rendered in panel (a) of Figure 1, the experimental set-up is a linear shear cell where a transparent plastic belt (6) rotates in an infinite loop to shear a viscous fluid confined in a small transparent tank (1). 
Two perpendicular cameras (7,8) are deployed to measure both particle projections in the x-y and x-z planes, displayed in panel (b).
A simple Computer Vision script based on the Canny method allows to detection of the object in each of the two frames, as shown in panel (c).
Having properly rescaled the measurements, the two projections are combined to determine the three-dimensional AABB of the given axisymmetrical particle.

The model is designed to be deployed during the post-processing of the experiments and it is trained on the geometry of the given particle. More in detail, closed expressions allow the calculation of the AABB of an oriented cylinder or ellipsoid, determining a convenient framework to generate synthetic data for the model training.

This methodology is applied to reconstruct the Jeffery Orbits (JO) of cylinders and ellipsoids suspended in a simple shear flow, in a viscous regime and when a small inertial effect on the particle becomes relevant.

Run the AABB_poseEstimation.ipynb on Google Colab for a quick demonstration.
