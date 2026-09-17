# A4 – Motor Mount

## Objective  

Design a motor mount using the (Brushed 24V DC Gear Motor 3.6Kg.cm/46RPM w/ 99.5:1 Planetary Gearbox) which attaches to a rigid wall.  

## Analyze  

For this design I began by getting rough estimates of the required dimensions based on the drawing of the motor. The diameter of the the indent that houses holds the motor was 18mm, so I knew the base and height would be more than that to accommodate. I used the same reasoning for the height, the shaft of the motor was 18mm long, so I knew the height needed to be less than that to give clearance to the shaft. I also made the decision to use PLA as my material.   

<img src="design_decision.jpg" alt="Description" width="50%">  

I then needed to design the two features of the mount. Feature 1 being the part that holds the motor and feature 2 being the part that is fixed to the wall. I was given a safety factor of 3, a force of 300N that would apply to the moment of the features, and a max deflection of 0.30mm for both features. An online datasheet gave me the values for the Elastic Modulus and yield strength of PLA.   

<img src="modulus_yield.png" alt="Description" width="40%">  

For feature 1, I assigned a rectangular geometry, and chose a length and height based on the dimensions of the motor. The third dimension, the base, would then be solved for using the beam bending equations for a cantilever beam. Also using the max stress and yield strength relation to safety factor to solve for max stress.  

<img src="Feature1_FBD.jpg" alt="Description" width="50%">  

I would need to solve for the base twice to find the actual minimum base required. Once considering the max stress and again considering the max deflection. The larger result of the two would need to be the minimum base of the rectangular feature.  

<img src="feature1_solve.jpg" alt="Description" width="50%">  

I found that the deflection was of greater consideration in this feature, so it determined the minimum base.  


## Decide


## Communicate

