# A11 – Motor Selection

## Objective
This assignment has us continuing to work with our groups to further design the tensile tester. This portion has us selecting a motor, designing a motor mount, designing/selecting a coupling, designing a floating bearing mount, and finalizing our assembly. We were given very few requirements for making it, so creative freedom is in our hands. The requirements we do have are that it has to have two lead screws, it should be able to transmit 2kN of force, it should have a speed range of 1-50 mm/min, it has a safety factor of 4, and lastly it should have at least a 18 inch lead screw height, designed for a bench top. We were also given a picture of what a bench top tensile tester looks like as guidance for where our end product should land.   
<img width="684" height="553" alt="image" src="https://github.com/user-attachments/assets/921708f8-c67f-4f83-8ff1-c3021666ea35" />  
## Motor Selection - Landon Toepfer  
I went looking online for DC motors, just looking to see if they had enough torque to be able to provide the load needed for the tester. After looking through a few I found one with a data sheet that showed it was able to provide enough torque at the bottom and top of our speed range. Its a drylin DC motor with gearbox from igus.com. The link is in our bill of materials. Below you will see what I took note of, specifically the datasheet graph that I used to determine if it was sufficient.  
<img width="804" height="432" alt="image" src="https://github.com/user-attachments/assets/42769fd9-4169-4db1-a23b-783eef95b25b" />  
## Motor Mount Design - Landon Toepfer
Now that I found a motor I thought was good, I had to figure out how to mount it to the frame. Luckily the company supplying the frame also has mounting screws that go into the slots on the frame, so I knew how big those holes would be. I also knew the size of the holes in the motor, which are M3, and the profile of their locations given in the data sheet. I decided that the screws going into the motor were going to have to be flat head screws with a countersink hole in order for them to have no profile on the bottom of the mount. This is important because they would be pressed up against the frame. The top of the mount has M8 holes for the frame assembly screws. I then just had to use bearing stress analysis to ensure that the thickness I wanted was larger than the thickness needed for the plate to not break. I used two new equations. One was solving for the force at each hole, It takes into account the total torque and the distance from it to each hole. I had an off center motor shaft, but I assumed it was in the center for this equation. Then the bearing stress was just like any other stress equation, having force over area. The difference is the area is the diameter times the depth, which is a projection of the actual area being affected. I don't understand why necessarily but that how the area is determined. I then was able to solve for the thickness and for both sets of holes, I got way less than 1mm. So I went with my chosen thickness, which was determined from the dimensions of my motor and moved into designing my mount in Creo.  
<img width="762" height="723" alt="image" src="https://github.com/user-attachments/assets/abcb4ccf-eabb-48af-8abf-8eec8c7a38cd" />   
<img width="775" height="546" alt="image" src="https://github.com/user-attachments/assets/6b57111a-9f3e-4ae4-9b33-997b774acefd" />  
## Coupling Design/Selection - Landon Toepfer
For this portion we had to either design a coupling or find a coupling. Whether you chose to design one or not you needed to prove that the one you had could resist breaking under torque. So I went ahead and found a coupling on amazon that worked. Found the material it was using and made an estimate of its shear strength. Then I was able to solve for the shear applied to this shape. I used a polar moment of inertia of a hollow shaft, knowing the inner and outer diameters. I calculated for both sides, one for the 6mm motor shaft, and the other for the 10mm screw. I ended up only getting around 1 MPa for both sides. So I was able to say it was strong enough to not shear.  
<img width="788" height="724" alt="image" src="https://github.com/user-attachments/assets/187dd08c-ed1c-4f77-bb46-b78e560d111b" />  
## Bracket design / frame confirmation - Jacob Shaver  
For this portion of the assignment, I was tasked to complete a strength analysis to confirm my desired bracket dimensions. The way that I did this was by finding bending stress on the bracket, bearing stress on the bracket's holes, and shear stress on each bolt in the bracket. I then took these values and compared them to the yield strength of the bracket, which I assumed to be the same material as my frame. To start the design process I first needed some bracket dimensions, and I decided to use the L-bracket found on the website below.  

Bracket Component link: https://www.grainger.com/product/80-20-Inside-Corner-Bracket-Inside-5JRP7  

<img width="776" height="599" alt="image" src="https://github.com/user-attachments/assets/f210f961-e0a4-4708-96c6-895268524e4d" />  

I used these dimensions to find all my stress values. Once I determined the values I went through and compared each to the yield strength of 172.37MPa and found a set of safety factors. My confirmation was, if all the safety factors exceeded my desired value of 4 then the bracket would hold. All of the stresses produced a very high safety factor with my lowest being 95.  

<img width="774" height="676" alt="image" src="https://github.com/user-attachments/assets/082e88a6-691c-46a3-a7e1-ac1f24ecb6f8" />  

## Verification of Top Bar Through FEA - Jacob Shaver  

Next I needed to confirm that the top of my frame would hold under the force from the leadscrews, and the torque from the motor. I did FEA through Creo PTC which had me first set up part fixtures and loads/moments. Most of this process was fine; however, when it came to implementing the torque reactions I had to get creative and turn it into a force couple because I couldn't figure out how to directly input the torque into the analysis.  

<img width="624" height="510" alt="image" src="https://github.com/user-attachments/assets/9b60970a-0473-4159-a7cd-e7fca4676926" />  

### FEA Analysis 1 & 2  

Once I set up the fixtures and loads, I created a mesh with an element size of 30mm to start and ran the first analysis. I moved the element size down to 20mm and ran a new static analysis, so that I could compare the results and test for convergence.  

For my stress the high-end was extremely high; however, this was a singularity and wouldn't reflect what would actually happen in the real world. Instead of taking that value, I used a tool in Creo to directly analyze the stress all over the part and came up with a max stress of 8.6MPa for the 30mm element analysis and 7.6 for the other. As you can see in the picture below, essentially the entire part was dark blue which showed me I consistently was on the low-end of my stress range. Between both analyses the stress did not end up converging. I used my determined max stresses and the material of the bar to determine my safety factor. Between the two analyses the safety factor also diverged.  

<img width="1088" height="484" alt="image" src="https://github.com/user-attachments/assets/8981de4e-a7e8-4a00-8d01-cba9c92c9833" />   

For my displacement, my max was extremely low on both analyses, which was a good sign. The max seemed to be concentrated at the center of the bar, while the ends were almost completely unaffected. Between the two analyses the displacement did converge. This interaction can be seen below.  

<img width="1093" height="486" alt="image" src="https://github.com/user-attachments/assets/117da5f1-d7bd-4ffa-931b-e26397979e55" />   

### FEA Analysis 2 & 3  

Since the first two analyses did not converge, I did a third analysis with even finer elements and compared it to the second. Between the second and third analysis, the only values that converged was the safety factor. Despite that my values were still well within a desirable range for displacement and max stress.  

<img width="1087" height="489" alt="image" src="https://github.com/user-attachments/assets/b1e73e76-9e7d-4795-950e-3837f62f13a9" />  

<img width="1090" height="489" alt="image" src="https://github.com/user-attachments/assets/0d41a04b-a624-4368-b1fe-18fd25102d37" />  

### Proposed Changes in the design   

<img width="691" height="490" alt="image" src="https://github.com/user-attachments/assets/82eeac77-5cac-41cd-96c9-0d00fa5b05fa" />

After analyzing the max displacement and max stress along with their locations, I think the spot to change is at the ends of the beam. One change that would lower some of the weight is to remove some material in the middle of the beam where it connects to the vertical one. Otherwise I think the original design is pretty good already and sufficient for what we need it to do.  

## Verification of Side Bars Through FEA - Jacob Shaver  

After running FEA on the top bar I needed to do the same for the vertical supporting bars. Because of symmetry, I knew the reactions in both vertical bars would be near-exact so I only did FEA on one. To do this I made fixtures where the bar would be held to another with a bracket, an axial compressive load on the top face, and a transverse load from the motor reactions on the top end of the vertical bar. This can be seen below.  

 <img width="246" height="623" alt="image" src="https://github.com/user-attachments/assets/13a63674-29ac-48eb-9efa-b60dfa69fc0b" />
 
### FEA Analysis 1 & 2  

After setting up the required fixed points and load points, I began the study by using a mesh of 20mm. Once I ran that study I did another with a mesh of 15mm.  

Once more, the high-end for my stress was leagues higher than my yield strength; however, this was a singularity that wouldn't directly reflect the real world. This is why I did the same thing as earlier and used a tool to find my max stress on the bar. The values for analysis one ended up being 0.8113MPa for the first and 0.8077MPa for the second. These two values converged when tested. I used these and compared them to the yield strength to find the safety factors, which were extremely high and converged.   

<img width="1090" height="486" alt="image" src="https://github.com/user-attachments/assets/c48dad25-2f06-4222-8ae2-79db2ccb6b9f" />  

For the displacement results, the max values were very low again. The max deflection was located at the upper left corner of the beam. Even though the max values were desirable, they did not end up converging.  

<img width="1090" height="489" alt="image" src="https://github.com/user-attachments/assets/c0e2f2cb-387b-4650-b2e8-d736e97483e2" />  

### FEA Analysis 2 & 3  

Since my displacement didn't converge I ran another pass with an even finer element size of 10mm and compared it to the second analysis. Between these two analyses, the stress and the safety factor converged but the displacement still didn't. However, my values were still well within what we needed for the frame to be stable under the set conditions.  
<img width="1088" height="486" alt="image" src="https://github.com/user-attachments/assets/cffdf331-00a0-43f2-8d6a-11c3892d67b2" />  
<img width="1089" height="485" alt="image" src="https://github.com/user-attachments/assets/50666fc2-e11e-4e55-8b02-049c92db79de" />  
### Proposed Changes in the design  

<img width="689" height="642" alt="image" src="https://github.com/user-attachments/assets/fa46d973-a3e1-4fb4-be1a-354e257e7fd2" />  

After analyzing the max displacement and max stress along with their locations, I think the spot to change is at the middle of the beams. One change that would lower some of the weight is to remove some material in the middle of the beam where it isn't being connected to another beam. This would greatly cut down on the weight of the beam, and as long as too much isn't removed, it shouldn't lower the safety factor too greatly. Otherwise I still believe the original design is pretty good already and sufficient for what we need it to do.  
## Final Assembly and Assembly Drawing - Jacob Shaver  

Below is the final assembly with all designed parts, and the drawing to go along with it.  

<img width="553" height="672" alt="image" src="https://github.com/user-attachments/assets/8c9b9085-8dfe-4e39-b2a4-b9f929f3eddf" />  

## Bearing Mount - Landon Toepfer  
I then had to design a floating bearing mount. I started by looking at other designs of what that would look like. It seems like its a housing for a bearing. So I went and found a bearing that I could put the screw into. I also assumed that The bottom of the lead screw could be ground down to get rid of the threads. I assumed I would machine the threads off down to 8mm diameter. So that is the diameter I used to select a bearing. Then after selecting a bearing I had measurements to design a housing around it. I had to use a RC3 fit to locate the screw so I made a top entry hole with that fit class using a 8mm nominal size. I had to do some convergence between mm and inches but it wasn't a big issue. I then just made it attach to a flat plate with the same sized screw holes as the motor mount. I went ahead and made it up in CAD, downloaded the CAD file for the bearing and handed it off to Jacob to put in the assembly. Below you will see my design work.  

<img width="716" height="673" alt="image" src="https://github.com/user-attachments/assets/fa01dc3d-4539-4f69-bbd5-f5fbf5b79fde" />  

## Bill of Materials - Landon Toepfer  
I just have to build off the table from the last assignment.  

| Item Number | Quantity | Name | Unit Price | Total Price | Purchase Link |
| --- | --- | --- | --- | --- | --- |
| 1 | 2 | Lead Screw | 23.67 | 47.34 | https://www.mcmaster.com/7549K72/ |
| 2 | 2 | Flange Nut | 73.36 | 146.72 | https://www.mcmaster.com/7549K16/ |
| 3 | 1 | Crosshead | - | - | - |
| 4 | 8 | Socket Head Screw | 10.43 (Pack of 25) | 10.43 | https://www.mcmaster.com/91251A550/ |
| 5 | 8 | Hex Nut | 3.60 (Pack of 50) | 3.60 | https://www.mcmaster.com/95479A111/ | 
| 6 | 1 | Frame | 143.40 (2m Worth) | 143.40 | https://www.grainger.com/product/80-20-T-Slot-Framing-System-Profiles-906T85 |
| 7 | 8 | Corner Bracket | 6.84 | 64.72 | https://www.grainger.com/product/80-20-Inside-Corner-Bracket-Inside-5JRP7 |
| 8 | 32 | Bracket Assembly Screw | 21.56 (Pack of 15) | 64.68 | https://www.grainger.com/product/80-20-Bolt-Assembly-M8-Size-5JRH6?opr=OAPD&analytics=relItems_5JRP7&position=1 | 
| 9 | 2 | Motor Mount | - | - | - | 
| 10 | 2 | Bearing Mount | - | - | - | 
| 11 | 2 | Motor | Unlisted (~80 estimated) | ~160 (allotted) | https://www.igus.com/product/drylin_E_AE_B_24_001 | 
| 12 | 12 | Motor M3 flat head screws | 7.34 (Pack of 100) | 7.34 | https://www.mcmaster.com/91294A132/ | 
| 13 | 2 | Bearing | 17.26 | 34.52 | https://www.mcmaster.com/1301N212/ | 
| 14 | 40 | Engineering Design Cost | 35/hr | 1400 | - | 

## Drawings
Here is the drawing of the motor mount:  
<img width="775" height="596" alt="image" src="https://github.com/user-attachments/assets/35a4c23a-88ca-45d2-ae15-e453ec20eef4" />  
Here is the drawing of the bearing mount:  
<img width="775" height="600" alt="image" src="https://github.com/user-attachments/assets/27d11b6d-13fc-400d-b97e-261c5bcc4b7d" />  
Here is the drawing of the assembly:  
<img width="774" height="492" alt="image" src="https://github.com/user-attachments/assets/689980ab-63b2-4316-b804-ae91892df2f3" />  
## Lessons Learned  

### Jacob
Throughout this I learned how to use Creo PTC to complete FEA’s. Last time Landon did the FEA portion so it was nice to learn how to do it this time around. Math-wise I don't think I learned much as it was a lot of pretty basic stress applications, and I’m already used to selecting standard parts after testing strength.  

### Landon  
I learned about bearing stress and how forces get transferred through fasteners. I had to use a few equations I was unfamiliar with. One thing I think I built on was my ability to understand how standardized components fit into custom projects like this. The assignment is showing me how to combine custom parts and standard parts in order to achieve a final product that theoretically is more than capable than the assignment asks for. Overall I don't think a lot of it was new but it was challenging.  
## Downloads
The part files are inside of the drawing zips
<a href="../../files/bearing_mount.drw.zip" download>  
    Download the bearing mount drawing
</a>  
<a href="../../files/motor_mount.drw.zip" download>  
    Download our motor mount drawing
</a>  
<a href="../../files/tens_test.drw.zip" download>  
    Download our assembly drawing
</a>  
<a href="../../files/tensile_test_final.asm.zip" download>  
    Download our assembly
</a>  





