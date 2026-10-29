# A8 – Gears

## Objective
-Design a gearbox that can be assembled and disassembled.  
-Analyze and size input and output shafts for strength.  
-Design journal bearings to support shafts.  
-Create a gearbox housing with proper clearance and fastening.  
-Use parametric CAD modeling to generate a final design.  
-Document calculations, sketches, and lessons learned.  


## Shaft Design  

The first step to this design was to confirm dimensions of shafts, one being a power transmission shaft that turns a pinion. The pinion turns a larger gear that turns a short shaft.  

Before I could confirm the validity of the given diameters of the shafts. I needed to use the gear ratio and given output speed and torque to find the resulting speed and torque that the power transmission shaft would need to input.  

<img src="shafts.jpg" width="50%" alt="Description of image">  

Now that the torque and speed of the power transmission shaft were found I could confirm that the given diameter 0.125in was acceptable in regards to the shear stress acting on the shaft.  

<img src="PTstress.jpg" width="50%" alt="Description of image">  

The value for the max stress (4000 psi) is generally used in practice for power transmission shafts and is listed in the Machinery's Handbook. I used 8500 psi for the short shaft, which is also listed in the Handbook.  

I used the same process to solve for the shear stress in the short shaft.  

<img src="SSstress.jpg" width="50%" alt="Description of image">  


## Journal Bearings  

The journal bearings would be placed between the shaft and holes of the gearbox to transmit fluid motion.  

The first step in the process was to determine an appropriate material to use for the bearings using the table from the Machinery's Handbook. To do this I would need to solve for the pressure that would be put on the bearing due to the turning of the gears, the surface velocity and the PV limit. I found the pressure by calculating the resultant of the tangential and radial force. The velocity I found earlier but needed to convert to feet/min.  

I solved for the power transmission bearing first.  

<img src="PTjournal.jpg" width="50%" alt="Description of image">  

I determined that Acetal was an appropriate because it met all the parameters.  

I then determined a length and diameter for the bearing. I was limited by the available parts for dimensions, but I solved for a clearance between the shaft and bearing, this clearance would allow for a thin layer of oil to reduce friction. I chose an RC4 fit because it was ideal for moderate loads and speeds while still providing accuracy and minimal play. The length was determined by the available Acetal bearings.  

<img src="PTJdia.jpg" width="50%" alt="Description of image">  

The same calculations were performed for the bearing that held the short shaft.  

<img src="SSjournal.jpg" width="50%" alt="Description of image">  

I realized after that it wasn't necessary to solve for the pressure again, because of equilibrium the forces acting on one gear would be equal and opposite the other and would result in the same value.  

The same process was used to find the clearance for this journal bearing.  

<img src="SSJdia.jpg" width="50%" alt="Description of image">  

The final design component for the bearings was to determine the minimum thickness of the journal bearings walls. The parts only came with certain thickness, most commonly 1/16" or 1/8". So I decided I would round up to the closest.  

I did this for each bearing and ended up using the same thickness 1/16" for each. I used the thickness to find the outer diameter of the bearings, which was also listed in the parts details.  

<img src="PTthick.jpg" width="50%" alt="Description of image">  
<img src="SSthick.jpg" width="50%" alt="Description of image">  

I used these calculations to choose proper bearings from McMaster-Carr.  

**Power Transmission Bearing:**  

<img src="PTbearing.png" width="50%" alt="Description of image">  

**Short Shaft Bearing:**  

<img src="SSbearing.png" width="50%" alt="Description of image">  


## Gearbox Design  

For the gearbox













## Decide


## Communicate

