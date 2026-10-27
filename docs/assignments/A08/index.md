# A8 – Gear Box Design

## Objective
In this assignment, we were tasked with designing a complete gearbox with one pinion and one gear. The assignment gave us the requirements of it has to be able to be disassembled. The output gear torque and speed are to be 1.25 in-lbf and 1100 rpm respectively. the input and output shaft diameters are .125 and .25 inches and each have a length of 1 inch.  

## Shaft Design  
I started by listing my knowns that were given to me in the problem and all of the unknowns that I would need to find including what the allowable stresses are on each shaft because part of this step is evaluating whether the shaft diameters chosen are suitable. I then went and found a bunch of equations that I thought I would need to solve the problem. I also looked at examples of shaft forces online to understand where the variables I'm solving for belong in a free body diagram. I then broke up my sheet with a dotted line and started to write out the equations algebraically before I actually solved them numerically. After I solved for what I wanted, I found the max stresses allowed for different shaft types in the book as 4000 psi for power transmitting which would be my input shaft and 8500 for small short shafts which I figured was my output shaft. Using these I found both shafts to be a suitable diameter.  
<img width="1338" height="1173" alt="image" src="https://github.com/user-attachments/assets/ccbfa2e1-c9d1-46f7-97a0-e98da54bdbc7" />  

## Journal Bearing Design
The second portion of this assignment has me designing the journal bearings. This mainly consists of solving for the pressure, velocity and the PV rating. Secondly, solving for the thickness of the bearings. The assignment does provide two specific gears to be used for this gear box from a supplier website that has integrated Solidworks models to download. I should be able to import these models to Creo. The specific gears are from McMaster-Carr and are the 7880K19 and 7880K24 20 degree metal spur gears. With this given I am able to know the pitch diameters, sizes, and thicknesses of these gears so I can properly design this gear box. I used the same process as in the last step of listing my knowns and my unknowns then finding the equations I would need to get there. I also drew a free body diagram of the bearings before solving. I solved the equations algebraically then numerically and was able to find my PV max that I would need to determine my material.  
<img width="957" height="1241" alt="image" src="https://github.com/user-attachments/assets/5dcb5c16-4175-42d0-a519-f393c5b65dff" />  
The other part of the journal bearings I have to solve for is the thickness of the bearings. I listed my knowns and unknowns and used a simple stress equation to determine the thickness needed. I used the Pmax of the material selected and drew a free body diagram in order to solve for the thickness of the bearing. I ended up getting 0.002 in. I then selected two bearings from the McMaster-Carr database that would end up being used for my gearbox and listed their part names at the bottom.  
<img width="1460" height="1079" alt="image" src="https://github.com/user-attachments/assets/1586fcc8-7d73-47e1-9d82-bd3a280a353a" />  

## Housing Design  
The assignment then asked me to sketch how this gearbox would look and be assembled. I came up with this design. It's a trapezoidal shape, it has internal shoulders to keep the bearings from moving inward. Lastly it is fastened with a nut and bolt system.  
<img width="1987" height="1095" alt="image" src="https://github.com/user-attachments/assets/26343cbf-0ab4-4329-8f39-ea64dcfa3b17" />  
Most of the parts I can import files for, like the gears, the bearings, and the nuts/bolts.


