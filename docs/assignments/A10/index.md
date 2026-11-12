# A10 – Lead Screw Translating System

## Objective

Design and build a mechanically driven tensile tester capable of applying up to 2 kN axial tensile load with a controllable crosshead speed from 1 to 50 mm/min.  

## Leadscrew Diameter, Speed, and Torque: Jack Welch  

To begin the selection of an appropriate lead screw, I solved for a minimum diameter that the screws needed to be to handle a maximum load. The load capacity of the tensile tester was to be 2kN, due to equilibrium each screw would be handling a load of 1 kN. From research I found that lead screws were mainly made from steel, so I used the yield strength for steel with a safety factor of 4 to determine an allowable stress.  

<img src="ls_dia.jpg" width="50%" alt="Description of image">  

I found the minimum diameter to be 0.21 in, from there I chose a lead screw with a minor diameter larger than that, and that was also available in McMaster, which I found to be the 3/8 - 12 thread size. From there I could use the lead to solve for speed and torque.  

<img src="lead_screw.png" width="50%" alt="Description of image">  

**CAD:**  
https://drive.google.com/file/d/163GmhDvFf3Nv7je6vWIuRtuG2nsFpk1d/view?usp=sharing  


From there I found the range of rotational speeds from the linear speed by using the lead length of 0.083 in.  

<img src="ls_speed.jpg" width="50%" alt="Description of image">  

Then I found the torque using the load, pitch radius of the lead screw, the lead, and the coefficient of friction between the steel lead screw and the 673 bronze nut.  

<img src="ls_torque.jpg" width="50%" alt="Description of image">  

## Selecting a Nut and Flange: Jack Welch

From the lead screw I was able to choose a corresponding bronze nut and steel flange that all fit together.  

<img src="nut.png" width="50%" alt="Description of image">  
<img src="flange.png" width="50%" alt="Description of image">  

**CAD:**  
https://drive.google.com/file/d/1JBb-zT3Mmm7f8CN-EyB0Ai5qbnt2cNWp/view?usp=sharing  

https://drive.google.com/file/d/1-kg0XealJPAPcINVkkOLJUTcmPzSoKX4/view?usp=sharing  

Before I could confirm the use of the nut and flange, I needed to verify that the internal threading would be able to handle the 1 kN load, I already figured this would not be an issue considering I chose the 12 thread nut and screw.  

<img src="nut_verify.jpg" width="50%" alt="Description of image">   


## Design the Crosshead - Saniyah Wilson  
### Research - Saniyah Wilson  
  
Before beginning analysis, I researched existing bench-top footprint tensile testing machines and the given load cell to determine the length of the crosshead. The main issue of the area or size of the head is ensuring all parts have room to fit and function on the part. To do this, I found the sum of the two nut flange diameters and the width of the cell to find the length if each part was tangent to each other. Then, using a sketch, I chose gap distances between the parts/features. This total is my chosen length.  
  
Since the nut flange was found to be 1.6 inches, I used that diameter as the minimum base measurement for the crosshead. Since it is a minimum, and FEA is to be conducted later, I chose to dimension the design for part at 2 inches instead.  
  
Lastly, I chose 1090 Steel as it is a tool steel with high strength and should result in a durable part.  

**Resources:**  
- https://www.azom.com/article.aspx?ArticleID=6560   
- https://www.azom.com/equipment-details.aspx?EquipID=5618   
- https://repositum.tuwien.at/bitstream/20.500.12708/200949/1/Demmel%20Stella%20-%202024%20-%20Design%20manufacturing%20and%20testing%20of%20an%20open-source...pdf  
- https://assets.dwyeromega.com/spec/DS-LC103B.pdf  

### Beam Stress/Strength Analysis - Saniyah Wilson  
  
The only dimension left unknown is the minimum height, or thickness, of the crosshead. To determine this I conducted a Beam Stress and Strength Analysis assuming the lead screws act as supports. In these calculations, the relationship between stress, yield strength, and section modulus are used to determine the unknown measurement.  
   
Once the final formula has been found symbolically, numbers are input and the value is solved numerically.  
  
**Visuals:**   
  
<img src="L10STRENGTH.jpg" alt="Description of image" width="50%">  
<img src="L10STRENGTH2.jpg" alt="Description of image" width="50%">  
<img src="L10STRENGTH3.jpg" alt="Description of image" width="50%">  
  
### Beam Deflection Analysis - Saniyah Wilson  
  
Next, beam deflection analysis is conducted to compare the results to the first found value. It can be noted that the Yung's Modulus of 1090 Steel is added to the list of known values in GPa. I chose to do the calculations for this analysis using metric dimensions because the given maximum deflection to be used, 0.01mm, is a much smaller magnitude once converted. Chosen measurements are converted as well for the same reasons.  
  
Here, the relationship between that maximum deflection, the Yung's Modulus, and the moment of inertia are used to find the unknown measurement. Once found numerically, it is clear that the first found measurement is the true minimum.  

**Visuals:**  

<img src="L10DEFLECTION.jpg" alt="Description of image" width="50%">  
<img src="L10DEFLECTION3.jpg" alt="Description of image" width="50%">  
<img src="L10DEFLECTION4.jpg" alt="Description of image" width="50%">  
  
### Final Height Chosen - Saniyah Wilson
    
These dimensions are fairly low due to the choice to use a very strong steel, so I chose the height at one inch. This choice makes the part more realistic to manufacture.  
    
<img src="FINAL HEIGHT.jpg" alt="Description of image" width="50%">  
  
### Initial Paper Drawing  - Saniyah Wilson

<img src="A10 Sketch_1.JPG" alt="Description of image" width="50%">  


### Tabulating Costs - Saniyah Wilson  
  
Total costs of each part our team did not design, but were used in the final assembly,
were tabulated here.  
  
<img src="L10COSTS.png" alt="Description of image" width="50%">   
  
**See the Parts Yourself:** https://docs.google.com/document/d/1bKbhDkLOe-WH6ZnaHG-k7sk0W9YO7X9axeHdGJF9zss/edit?usp=sharing   


## Assembly Modeling: Jack Welch  

To begin the assembly of the tensile tester, I decided on a T-slot frame. On the Grainger resource, the only parts with CAD downloads were 3 meters long, so I chose one and shortened it too 920mm, this would be just over the 3 foot lead screws it was meant to frame. The frame parts I chose have a 40mm by 80mm base, and I used four of them to construct the top, bottom and sides of the frame.  

<img src="frame1.png" width="50%" alt="Description of image">  

I decided to create small holders for the lead screws on the top and bottom of the tester, I made them simple 2in x 2in squares with a 0.375 in hole to fit the screws.  

<img src="screwhold.png" width="50%" alt="Description of image">  

I fixed these holders on the top and bottom of the frame and slid the lead screws into the holders.  

<img src="frame2.png" width="50%" alt="Description of image">  

Next I assemble the nuts and flanges, and slid those onto the lead screws.  

<img src="frame3.png" width="50%" alt="Description of image">  

Finally, I mated the finalized and optimized crosshead onto the flanges, which set the distance between the lead screws.  

<img src="frame4.png" width="50%" alt="Description of image">  


**CAD:**  
**Assembly:** https://drive.google.com/file/d/1HjdAu9P-SXngTeJbTKmL_nTZw0w4PDA-/view?usp=sharing  

**Frame:** https://drive.google.com/file/d/1HbYq9SuitAdi3XTQkz1fmQAPXDYvJJVo/view?usp=sharing  

**Screw Mount:** https://drive.google.com/file/d/14MdHZLryXikqc4SRxZua57EihbCsW9tF/view?usp=sharing  


## Parametric CAD Model of Crosshead - Saniyah Wilson
### Initial Design - Saniyah Wilson

Following the initial sketch the dimensions chosen were input into the global equations system in SolidWorks. I chose to leave dimensions which were related to outside parts or which would not be used in the end geometry to be added to the equations throughout the modeling process. This way, variable names are not overly reused, eliminating some confusion.  


<img src="A10PARA.png" alt="Description of image" width="50%">  
The model begins with a rectangle at the base and length determined and is extruded to an inch.   

<img src="A10CAD1.png" alt="Description of image" width="50%">  
  
On one side, the hole for the lead screw is designed and mirrored to the other half of the part. Then, a cut extrude is used to remove the material.    
  
<img src="A10CAD2.png" alt="Description of image" width="50%">  
<img src="A10CAD3.png" alt="Description of image" width="50%">  
<img src="L10CAD4.png" alt="Description of image" width="50%">  
    
To create the bore holes to mount the crosshead to the flange, I used the measurements referenced and created a concentric circle around the lead hole. This circle is used to align the holes and then is cut before they are mirrored to the other side.   
  
<img src="L10CAD5.png" alt="Description of image" width="50%">  
<img src="L10CAD6.png" alt="Description of image" width="50%">   
  
Lastly, a cut extrude creates eight holes at half the thickness of the crosshead. This completes the initial model, which I then passed on to Jack for FEA analysis.   
  
<img src="L10CAD7.png" alt="Description of image" width="50%">  
<img src="L10CAD8.png" alt="Description of image" width="50%">  

**Final Model and Parametric Values Added**  
  
<img src="L10FINALCAD.png" alt="Description of image" width="50%">   
<img src="L10FINALPARA.png" alt="Description of image" width="50%">   
      
**Download the File:** https://drive.google.com/file/d/1dN-fcCupNEkCIPUpsWeFSNqFMlzsTfWq/view?usp=sharing  


## FEA Analysis: Jack Welch  

For the first FEA, we used a simple crosshead. I set the fixed supports at the holes that would attach the flanges to the crosshead, and made a concentration in the middle of the crosshead for the 2kN force that would be applied.  

<img src="rigid.png" width="50%" alt="Description of image"> <img src="force.png" width="50%" alt="Description of image">  

I started with a default mesh and ran the study, because of our desire to dimension the crosshead with a height much greater than the minimum, the results for stress, displacement and safety factor were all ideal.  

<img src="FEA(1SF).png" width="50%" alt="Description of image"> <img src="FEA(1d).png" width="50%" alt="Description of image"> <img src="FEA(1s).png" width="50%" alt="Description of image">  

Then I increased the mesh size and ran the study again, the only value that had a considerable convergence was the max stress, which is because the stress was concentrated in a small area on the innermost fixed holes.  

<img src="FEA1.jpg" width="50%" alt="Description of image">   


## FEA 1 Optimization of Crosshead - Saniyah Wilson
  
Because the results I received from Jack showed both low stress and deformation and a high safety factor, I focused on minor changes which would decrease the overall weight of the part.  
  
I began by chamfering the outer edges of the part at 0.5 in to avoid entirely cutting out the 0.1 inch gap I added between the flange and the shorter side of the part. Next, I created an extruded cut which is equivalent in diameter to the flanges chosen, so that they sit further within the model. This was cut to an arbitrary height below the height of the mount holes, to hopefully avoid interference there as well.  
  
**Visuals:**  
  
<img src="L11FEA.png" alt="Description of image" width="50%">  
<img src="L11FEA2.png" alt="Description of image" width="50%">  
<img src="L11FEA3.png" alt="Description of image" width="50%">  
  
## Final FEA - Saniyah Wilson
  
With the revised model finished, I moved into the second round of FEA. I ran the statics study through SolidWorks, representing the force as a center cluster of forces in the center. Both a medium mesh and fine mesh were used for the analysis and the results were compared. This data converged, so I found it unnecessary to continue to make changes to already revised geometry of the crosshead.  
  
**Results:** _Table created by Jack Welch_  
  
<img src="A10FEA2.jpg" alt="Description of image" width="50%">  
  
**Download Final Part:** https://drive.google.com/file/d/1j0eWfDDwDiHvawwkSNXH4fF1OZJwJ8fr/view?usp=sharing  
  


## Drawing: Jack Welch  

<img src="crosshead_draw.png" width="50%" alt="Description of image">  



**CAD:**  https://drive.google.com/file/d/1RzKMhPNEgwyBx3Y7eFhDD15VWFP3zDZO/view?usp=sharing  



## Lessons Learned: Jack Welch  

I learned how torque, speed, and an axial load inform decisions for choosing lead screws, and how a nut, flange and lead screw interact to translate force and movement. I also learned how many different sizes of lead screws are available and now have an estimate for sizes based on force. Additionally, I learned more about lead, pitch, and the different diameters of screws and threaded holes. I spent about 12-13 hours on this assignment.   

## Lessons Learned - Saniyah Wilson  
  
**Time to Finish:** 13 hours.  
  
Through this assignment, I learned how a lead screw can be used to apply a force to a designed structure. I gained a better understanding of using beam simplifications in a functional design as well. I did not realize that the lead screws could be assumed to act as the supports for the "beam."  
  
Additionally, there was insight in the values I found from those calculations. I found an incredibly small minimum height, which I believe was due to the 1090 Steel chosen for the part. In the future, I will more thoroughly consider all elements of the material in connection to the parts function. For this assignment, I was largely focused on strength and did not consider the other material properties as closely.  
  
Finally, in the CAD process, I found that my parametric modeling process worked well and improved my ability to properly track where variables were used throughout the model. In the past I've struggled with similar variable names or entirely missing parametric values. By continuing the parametric process in CAD, no values were missed and names were able to stay unique.  










