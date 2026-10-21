# A7 – FEA on Bracket

## Objective  
In this assignment I was tasked with performing an iterative testing process on the bracket from the previous assignments. This process including an inner loop and an outer loop. The inner loop contains most of the work. To complete the inner loop I have to: set up the constraint and loading on the bracket, determine the mesh definition, test the bracket, and then repeat until the results converge within 7% or it is the third attempt to converge. To complete the outer loop, I do the inner loop and then once I have converged results, I make an informed change to the design. Once I've made two changes and ran three inner loops the assignment is complete. To start I opened my bracket file from the previous assignment and set up the material properties for the Aluminum used.  
<img width="737" height="593" alt="image" src="https://github.com/user-attachments/assets/85c48691-9f29-4de9-8ff1-d2bbae7a19ba" />  
Then Creo automatically translated the units into the ones used to define the model. Which would be psi, or pounds per square inch. I then moved into defining the constraints. For this bracket, its where the T beam would be contacting so its all of the inner surfaces that had a specified fit in the previous assignment.  
<img width="1083" height="599" alt="image" src="https://github.com/user-attachments/assets/d9049c20-9f24-4252-8465-8248b642ef50" />  
I then defined where the force is pulling on the bracket. So I selected the rod on the bottom, or feature A. I then can use the coordinate system which is shown in the bottom right to figure out which coordinate direction I need to the force to be in. The force magnitude is 1400 lbf because the assignment showed to equal forces pulling down and I chose them to equal 700 lbf. The force needs to be pulling down so I have to input -1400 lbf in the y coordinate. You can see this below.  
<img width="778" height="683" alt="image" src="https://github.com/user-attachments/assets/a7071809-936d-436d-a842-a1b69b4b0590" />  
<img width="891" height="603" alt="image" src="https://github.com/user-attachments/assets/56a73d02-285c-4b9a-9ae2-b7def38e58f5" />  
I needed to do a few more things before I can run the simulation. I needed to assign the material to the bracket. I needed to allocate ram to the study process. Lastly I needed to define the mesh. I took a snip of what those first two menus look like.  
<img width="546" height="351" alt="image" src="https://github.com/user-attachments/assets/d468e4c9-a05a-4232-894e-0c465e25c15a" />  
Lastly defining the mesh in Creo means setting a maximum element size for each generated element. I had a general idea on how big they would need to be for a low amount of elements because I knew the general size of my bracket. I started with 1 in.  
<img width="1089" height="594" alt="image" src="https://github.com/user-attachments/assets/ef2ef599-755e-4840-a47b-9cbe81ba48dc" />  
## Inner loop 1  
Now that preprocessing is done, I'm running a single-pass adaptive analysis. Creo can run a multi-pass analysis to automatically check for convergence but it just generated more in depth equations in stead of increasing the amount of elements so it is not used for this assignment. Here is what the menu looks like, I didn't have to adjust any settings or anything.  
<img width="515" height="820" alt="image" src="https://github.com/user-attachments/assets/b1270406-c639-4c08-a661-1571db047e54" />  
I then ran two analysis to compare and check for convergence. The second one used 0.5 in elements.  
<img width="1238" height="525" alt="image" src="https://github.com/user-attachments/assets/eb6a2e6d-47dc-4b6d-b41b-883aa9dd87ef" />  
Here are the amount of elements for the first two tests.  
<img width="1048" height="410" alt="image" src="https://github.com/user-attachments/assets/b15ea7a2-59b9-427c-86fa-c41ee42269ae" />  
Here are what the studies look like for stress and dislocation side by side.  
<img width="1245" height="565" alt="image" src="https://github.com/user-attachments/assets/7afcb35f-e2fc-464e-9311-883554006ff0" />  
<img width="1247" height="602" alt="image" src="https://github.com/user-attachments/assets/1396e799-95d9-43fc-b582-c4075309bd37" />  
I then calculated the convergence on these two tests and I got a 9.6 percent so I had to refine the mesh.  
<img width="1046" height="227" alt="image" src="https://github.com/user-attachments/assets/b60249c0-f3cd-4e64-a052-4a2a60a6d3a6" />  
I went to do another with an element size of .25 in.  
<img width="1248" height="605" alt="image" src="https://github.com/user-attachments/assets/0387b9dd-a56b-4784-be36-eb39bd183a02" />  
This test had 54021 elements. Here are the results comparing tests 2 and 3.  
<img width="1244" height="597" alt="image" src="https://github.com/user-attachments/assets/8c68ed7c-9869-45bd-b200-d3172b82f85c" />  
<img width="1242" height="579" alt="image" src="https://github.com/user-attachments/assets/23d752a5-6f7a-48cd-9f96-1fef82c0dbe6" />  
I then tested for convergence and got 23.5 percent, so the results diverged and I will need to refine the mesh.  
<img width="1015" height="223" alt="image" src="https://github.com/user-attachments/assets/e329e10e-a769-40bb-9057-6b2d6546580d" />  
I refined the next mesh to an element size of 0.2 in because 0.125 was attempted and it was too large of a result for my current free space on my drive.  
<img width="1005" height="389" alt="image" src="https://github.com/user-attachments/assets/8b080476-dc9d-4fed-ad51-619a41a51e0e" />  
This test had 87981 elements. Here are the results comparing tests 3 and 4.  
<img width="1243" height="600" alt="image" src="https://github.com/user-attachments/assets/1f94e060-1df5-44bd-a166-3cf89cbb38ec" />  
<img width="1242" height="596" alt="image" src="https://github.com/user-attachments/assets/7ee52fe8-73fb-4025-8961-3923c7b45719" />  
I ended up getting a 3.28 percent convergence which is nice. I then was able to calculate everything I would need for my table for this first design. These values are the max stress and its location, the max dislocation and its location. The number of elements used which would be the most recent value. The mass and the safety factor which is obtained by dividing the stress or dislocation by the amount of maximum allowable stress or dislocation. Below is the calculation for the safety factor and what the menu looks like for the mass analysis.  
<img width="1041" height="221" alt="image" src="https://github.com/user-attachments/assets/ea7b29fd-b859-4df5-a5f8-11b53317b0e0" />  
<img width="621" height="655" alt="image" src="https://github.com/user-attachments/assets/73e95d71-a64c-4ee5-bf43-5d1f7702027d" />  
I then needed to calculate from the mass units provided into pounds so I looked up the conversion value.  
<img width="647" height="124" alt="image" src="https://github.com/user-attachments/assets/799b4a2e-4003-4585-8665-0ea9e8ced649" />  
## Inner loop 2  
I then made an informed change to my design. I added another support for the rod and rounded those corners to stop stress from concentrating. The rounding also helped support that bar more.  
<img width="584" height="723" alt="image" src="https://github.com/user-attachments/assets/0c6daaba-4c2f-4dcd-8bd5-bdf0533e3d75" />  
<img width="608" height="746" alt="image" src="https://github.com/user-attachments/assets/0fb8b19b-c1c2-4c33-a654-781d6ed1914a" />  
I won't be showing every step again for redundancy similar to how I only showed the report for how many elements there are once. I then ran the first two tests again, with 1 in elements giving me 2563 elements, and 0.5 in elements giving me 12956 elements.  
<img width="1087" height="536" alt="image" src="https://github.com/user-attachments/assets/cdd0ab29-0f9e-4acb-921f-1b0437b52aec" />  
<img width="1088" height="524" alt="image" src="https://github.com/user-attachments/assets/9f1861f6-514b-41d7-bc60-86affe40082e" />  
I got a 40.2 percent convergence so I ran another test with 0.25 in elements, giving me 61818 elements.  
<img width="918" height="397" alt="image" src="https://github.com/user-attachments/assets/aba0a9d0-9bc0-4e92-818f-527df6b6d804" />
Here are the results comparing tests 2 and 3.  
<img width="1090" height="528" alt="image" src="https://github.com/user-attachments/assets/d2e7af86-0eb4-4e52-8606-006b8576462d" />  
<img width="1088" height="524" alt="image" src="https://github.com/user-attachments/assets/6f734e49-0b31-468a-8248-0894da4683bb" />  
I got a 26.3 percent convergence so I had to run another test with 0.2 in elements, giving me 99248 elements.  
<img width="905" height="204" alt="image" src="https://github.com/user-attachments/assets/4285086b-c723-471e-9367-9e63c0ceeb8d" />  
Here are the results comparing tests 3 and 4.  
<img width="1086" height="534" alt="image" src="https://github.com/user-attachments/assets/ef14d16f-173e-4ddc-9743-686c1289a9d6" />  
<img width="1089" height="520" alt="image" src="https://github.com/user-attachments/assets/6cd83777-a0df-4c7f-8713-423f3176068d" />  
Here I got a 3.12 percent convergence.  
<img width="874" height="199" alt="image" src="https://github.com/user-attachments/assets/42c44645-fe41-4b0c-9586-942f22f314e4" />  
Now I can calculate all the values I need for my table. You will see the final table at the end of the third inner loop. I calculated the safety factors for stress and displacement.  
<img width="857" height="192" alt="image" src="https://github.com/user-attachments/assets/cd9a34e2-47de-4655-afc4-5031d9c3d78b" />  
<img width="834" height="206" alt="image" src="https://github.com/user-attachments/assets/bbe2e8b6-a033-49d0-a458-d802f2643f07" />  
## Inner loop 3
I then made a change to my design. Stress was still concentrating in the corner under the lip connecting features B to C so I rounded that inner corner and I increased the rounding on the bottom where is connects to the bar to decrease the bending in that bar and increase the support for it.  
<img width="772" height="614" alt="image" src="https://github.com/user-attachments/assets/cf3286b5-fb69-48ef-af90-ec36421fb421" />  
<img width="832" height="670" alt="image" src="https://github.com/user-attachments/assets/e203f0f2-b372-4eb7-9915-f15bdf45d54b" />  
I ran the first two tests again with 1 in elements giving me 2556 elements and 0.5 in elements giving me 12872 elements.  
<img width="1088" height="520" alt="image" src="https://github.com/user-attachments/assets/70cd5796-b66c-442d-8077-625fe497896f" />  
<img width="1085" height="580" alt="image" src="https://github.com/user-attachments/assets/04cb6a07-171d-4fc5-81c9-ee288dbafefa" />  
My results converged with 2.78 percent immediately which is super nice. So I just calculated my safety factors for stress and dislocation.  
<img width="847" height="204" alt="image" src="https://github.com/user-attachments/assets/e5119ec8-5610-4ac5-9cfc-e40896a9957f" />  
<img width="831" height="206" alt="image" src="https://github.com/user-attachments/assets/08192039-00b0-4313-ba08-748f75f09474" />  
## End of outer loop
So here are my results from my table. This shows how my informed changes increased the safety factors by decreasing the stress and dislocation. This improved the design measurably. I didn't try to optimize for weight in this process as adding new features was going to increase weight anyway. I essentially took a failing, theoretical design and tested it in Creo to find out how to turn it into a practical successful design.  
<img width="1033" height="521" alt="image" src="https://github.com/user-attachments/assets/3c029318-02ce-40ff-b9c7-4108767fee29" />  




## Analyze


## Decide


## Communicate

