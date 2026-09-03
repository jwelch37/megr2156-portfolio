# A2 – Truss Stress Analysis

## Objective
-Design a lightweight planar truss using A500 steel or an alternative material.  
-Create free body diagrams (FBDs) for joints and critical pins.  
-Calculate the required cross-sectional area of truss elements with a safety factor.  
-Determine pin sizes based on shear forces with a safety factor.  
-Solve equations symbolically and numerically for both truss and pin design.  
-Estimate the total weight of the truss and pins.  
-Create a CAD model with accurate dimensions and connections.  
-Compare CAD weight predictions with hand calculations.  
-Document key engineering lessons learned from the process.  

## Analyze  
# Designing the Truss  
For my truss, I decided to use a simple design that consisted of only right triangles, which would allow for easier calculations.  
<img src="1000001187.jpg" alt="Alt Text" width="50%">  

Next was to find the internal forces in each of the members, the goal being to find the maximum internal force, so I could later find the minimum cross-sectional area. First, I had to find the support reactions at pin A and roller B, the vertical reaction at B being of the most importance, because it allowed me to begin solving for forces at joint B.  
<img src="1000001190.jpg" alt="Alt Text" width="50%">  

Then I solved for all of the internal forces method of joints. Drawing a FBD of every joint.  

<img src="1000001193.jpg" alt="Alt Text" width="50%"> <img src="1000001196.jpg" alt="Alt Text" width="50%">  

# Determining Minimum Cross-Sectional Area of the Members  

The next step was to calculate the minimum cross-sectional area of the members that would support the 20KN loads. I did this by relating the formula for stress with the relation between the yield strength and a given safety factor of 3.5. I also calculated the approximate weight of the truss, I calculated the members all separately, grouping them if they were identical. I found the weight by multiplying the length of the member, by its cross-sectional area and density. I found the weight to be 12.283 kg, as can be seen below. I found the density of A500 steel here:  (https://beamdimensions.com/materials/Steel/ASTM/ASTM_A500/)  
<img src="1000001199.jpg" alt="Alt Text" width="50%">  


The yield strength for A500 steel is 345 MPa, which is info I found online at (https://www.tottentubes.com/astm-a500-specification-information).  
<img src="yield.png" alt="Alt Text" width="50%">  
I decided on using grade C because I read that it was most commonly used in construction.  



## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

## Communicate

