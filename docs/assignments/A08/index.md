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

The final design component for the bearings was to determine the minimum thickness of the journal bearings walls. The parts only came with certain thickness, most commonly 1/16" or 1/8". So I decided I would round up to the closest. I found the formula in the Machinery's Handbook and the allowable stress of Acetal online.  

I did this for each bearing and ended up using the same thickness 1/16" for each. I used the thickness to find the outer diameter of the bearings, which was also listed in the parts details.  

<img src="PTthick.jpg" width="50%" alt="Description of image">  
<img src="SSthick.jpg" width="50%" alt="Description of image">  

I used these calculations to choose proper bearings from McMaster-Carr.  

**Power Transmission Bearing:**  

<img src="PTbearing.png" width="50%" alt="Description of image">  

**Short Shaft Bearing:**  

<img src="SSbearing.png" width="50%" alt="Description of image">  



## Gearbox Design  

Initial sketch of design:

<img src="1000001518.jpg" width="50%" alt="Description of image">  

Before I started modeling, I created parametric equations of all the dimensions I thought I would need. I did not end up using them all, but most of them were important to the modeling, especially the pitch diameters.  

<img src="para.png" width="50%" alt="Description of image">  

For the gearbox I based the design around the circular shapes of the gears, with the starting dimensions being the pitch diameters. I made two tangential circles with diameters matching the pitch diameters of the gear and pinion.  

<img src="pitch_dia.png" width="50%" alt="Description of image">  

I would refer to the midpoints of these circles later in the design to cut the holes for the shafts and bearings. This would ensure the gear and pinions were the proper distance from one another. First I offset these circles to make room and give clearance for the gears, then extruded the whole shape at a draft and made a shell.  

<img src="shell.png" width="50%" alt="Description of image">  

I then added a lip around the top edge of the shell where I could place bolt holes to connect the top and bottom of the gearbox.  

<img src="lip.png" width="50%" alt="Description of image">  

I then made the sketch for the hole cuts based on the midpoints of the circles from before. The material I made ASTM A36 Steel. I also added the bolt holes to each end.  

<img src="wrong_holes.png" width="50%" alt="Description of image"> <img src="holes+steel" width="50%" alt="Description of image">  

I did not realize until the assembly that I had made the hole for the power transmission based on the diameter of the shaft instead of the outer diameter of the bearings, so I went back and fixed them.  

<img src="correct_holes.png" width="50%" alt="Description of image">  

Next, I added extrusions around the holes, the idea behind them was to limit friction between the gears and the bottom of the housing.  

<img src="final_bottom.png" width="50%" alt="Description of image">  

Finally, I created a lid of the same shape and bolt hole position, but shorter, as the gears did not need more space.  

<img src="final_bottom.png" width="50%" alt="Description of image">  

I created an assembly of the shafts which I modeled in the same ASTM A36 Steel, the housing, the gears and the bearings. The bearings and gears were downloaded from McMaster-Carr.  

<img src="assembly_gears.png" width="50%" alt="Description of image"> <img src="assembly_side.png" width="50%" alt="Description of image"> 
<img src="final_assembly.png" width="50%" alt="Description of image">   

## Part Drawings  

<img src="assembledraw.png" width="70%" alt="Description of image"> <img src="bottomdraw.png" width="70%" alt="Description of image"> <img src="topdraw.png" width="70%" alt="Description of image"> <img src="SSdraw.png" width="70%" alt="Description of image"> <img src="PTdraw.png" width="70%" alt="Description of image"> <img src="SSbearingdraw.png" width="70%" alt="Description of image"> <img src="PTbearingdraw.png" width="70%" alt="Description of image"> 



## Lessons Learned  

I learned a lot about how gears work in this assignment, especially about how precise they are and the amount of components involved in creating functional gears. Especially the important function of journal bearings in gear assemblies, which I was unaware of. The idea of power transmission and how the forces between the gears interact to transmit power was new to me. I also learned more about fits while designing the interactions between the shaft and bearings and the bearings to the housing.  

**CAD Files:**  
Assembly: https://drive.google.com/file/d/1VU1wOduhiFH9zjBCs3mrTO8EneAIhb-k/view?usp=sharing  
Gearbox bottom: https://drive.google.com/file/d/1YCzWUe-NrTiShCoLEJ3cFtJvJyqXWC5L/view?usp=sharing  
Gearbox Top: https://drive.google.com/file/d/12WfqkQMTVJSOiCeRtyElpUulEFFUeVSS/view?usp=sharing  
PT shaft: https://drive.google.com/file/d/1Mk_fvWxjjkPvHZ-oXRZeQVW72WdqcL4O/view?usp=sharing  
Short Shaft: https://drive.google.com/file/d/1MdZMg481pz0g-WdSJXjKAmK2fAfebPea/view?usp=sharing  



**Resources:**  
https://www.mcmaster.com/7880K24/  
https://www.mcmaster.com/7880K19/  
https://www.mcmaster.com/2610T2/  
https://www.mcmaster.com/2610T5/  
https://www.directplastics.co.uk/pdf/datasheets/Acetal%20Data%20Sheet.pdf  





