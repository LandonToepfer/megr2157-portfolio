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
The assignment seems like it wants me to make the sleeve bearings that I calculated so I will make those anyway. Here is the output bearing.
<img width="1064" height="933" alt="image" src="https://github.com/user-attachments/assets/4d228ced-e54c-4488-9f20-948b699dbf32" />  
And here is the input bearing.  
<img width="664" height="561" alt="image" src="https://github.com/user-attachments/assets/4441809e-749c-44a9-af78-96f31de548be" />  

## Housing Design  
The assignment then asked me to sketch how this gearbox would look and be assembled. I came up with this design. It's a trapezoidal shape, it has internal shoulders to keep the bearings from moving inward. Lastly it is fastened with a nut and bolt system.  
<img width="1987" height="1095" alt="image" src="https://github.com/user-attachments/assets/26343cbf-0ab4-4329-8f39-ea64dcfa3b17" />  
Most of the parts I can import files for, like the gears, the bearings, and the nuts/bolts. So I'll show you the ones I was able to import. My input bearing, output bearing, input gear, output gear, the screw and the nut.   
<img width="1391" height="938" alt="image" src="https://github.com/user-attachments/assets/bb14f71a-8566-4f0d-8839-9ed7c712cf93" />  
<img width="1745" height="1036" alt="image" src="https://github.com/user-attachments/assets/bbf79f73-e115-4205-a1ac-9ea466af65e3" />  
<img width="1553" height="1062" alt="image" src="https://github.com/user-attachments/assets/f9dfbcd4-4818-448d-9912-4a7278d86e69" />  
<img width="1354" height="966" alt="image" src="https://github.com/user-attachments/assets/50af79fd-287e-4bb2-8ad7-20b9021e0b31" />  
<img width="1200" height="791" alt="image" src="https://github.com/user-attachments/assets/357053d7-c66b-4f64-9cf0-18bcc94548c5" />  
<img width="1259" height="903" alt="image" src="https://github.com/user-attachments/assets/7faa0d95-30b1-4dc0-baf0-70f70ba51dbd" />  
I then designed my housing for the gears. I show you some of the parameters I set to design it, alongside the final product then Ill explain what I did to come up with it.  
<img width="2220" height="856" alt="image" src="https://github.com/user-attachments/assets/21a19be0-f226-43df-aff9-4cc1d5e9abc4" />  
I started with trying to define the inner area where the gears will be with some outside area so they don't touch the walls. I had to use a lot of tangent and perpendicular lines. I was able to use my relations to define where the gears would be sitting and then make larger circles around that and connect them to get the shape I imagined in my sketch.  
<img width="1171" height="1174" alt="image" src="https://github.com/user-attachments/assets/14923a93-ad29-4610-8ff4-ea7037cb067d" />  
My next sketch layer was defining the outside area of the base where the screw holes would be able to go through. I went and looked through McMaster-Carr for screws that would work and came up with 1-64 socket head screws 0.5 in long. With this I was able to put in the size of the screw holes and define their positions using close by geometry.  
<img width="907" height="1021" alt="image" src="https://github.com/user-attachments/assets/72d925bc-c985-498c-acea-93529dba4901" />  
Lastly I just traced over the last two sketches to get the one that would be extruded.  
<img width="938" height="1001" alt="image" src="https://github.com/user-attachments/assets/a4342529-4e90-4c6d-ab59-4132b62911ab" />  
Once extruded I traced around the hole once and then again with a thickness of .05 inches to get my walls.  
<img width="1322" height="1033" alt="image" src="https://github.com/user-attachments/assets/decf731d-aa9b-45d2-acfa-efbe04708780" />  
I closed in the roof of it and went to make my hole for my bearing to sit in, slightly smaller than it so it would have interference to hold it in place.  
<img width="1214" height="933" alt="image" src="https://github.com/user-attachments/assets/c81a1744-9a0f-43e9-8843-a8bbaa21e14b" />  
I then went and made the inside shoulder with a hole wide enough for the shaft to go through +0.025 in of clearance.  
<img width="1621" height="758" alt="image" src="https://github.com/user-attachments/assets/71e0dc49-1c5b-4743-a62f-41c9d193bee0" />  
I then rounded it to make it stronger and smoother.  
<img width="1161" height="911" alt="image" src="https://github.com/user-attachments/assets/ebbfa0fc-c852-46a7-850a-75d7d5009125" />  
Then I just backed up a few steps and made the output half of the housing. The only difference being where the shaft enters and the hole's size as well as some counterbores for the screw heads to sit in.  
<img width="1228" height="920" alt="image" src="https://github.com/user-attachments/assets/f6dc6082-1f82-41db-9ed2-d84ed7802096" />  
## Assembly
I went ahead and put it all together and here is what the final product looks like.  
<img width="1318" height="864" alt="image" src="https://github.com/user-attachments/assets/9609c073-6e95-4090-b5d4-087015c9572c" />  
<img width="1574" height="1201" alt="image" src="https://github.com/user-attachments/assets/1f900f87-3422-4a5b-b5fa-6479e62f2669" />  
## Drawings  
I have extra work to do as usual so I have to make drawings on the six parts I made and the assembly.  
Here is the input bearing.  
<img width="1444" height="1118" alt="image" src="https://github.com/user-attachments/assets/748f3473-e263-47c4-a1c3-aac50e522c97" />  
Here is the output bearing.  
<img width="1439" height="1113" alt="image" src="https://github.com/user-attachments/assets/d462dc1d-3018-4214-9a65-8120ac41b9c3" />  
Here is the input shaft.  
<img width="1444" height="1111" alt="image" src="https://github.com/user-attachments/assets/56b892f5-3b99-4de8-9177-139b86f27092" />  
Here is the output shaft.  
<img width="1442" height="1112" alt="image" src="https://github.com/user-attachments/assets/043dd41b-a732-4e2b-b8f3-15b5254bc25b" />  
Here is the input housing.  
<img width="1283" height="992" alt="image" src="https://github.com/user-attachments/assets/35dedf62-7eb5-4233-8961-a6948e6db55b" />  








