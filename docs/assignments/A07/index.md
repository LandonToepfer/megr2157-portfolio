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
I then made an informed change to my design. I thickened and added another support for the rod and rounded those corners to stop stress from concentrating. The rounding also helped support that bar more.  
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
## FEA on Link
I always have extra work so I had to do the same process on the link. I had the same setup where I had to assign the material and make sure I was in the right units. I did have to setup the constraint and the loading because its a new part. I went with constraining the top hole that connects to the bracket and pulling down using the bottom hole that connects to the 1 in diameter rod. I used the same magnitude of forces too.   
<img width="1092" height="669" alt="image" src="https://github.com/user-attachments/assets/95afe715-448c-49c5-a85a-983c1bffd03d" />  
## Inner loop 1
I again started with 1 in elements and 0.5 in elements for the first two tests. Giving me 537 elements and 1234 elements.  
<img width="1025" height="689" alt="image" src="https://github.com/user-attachments/assets/34388ad2-3449-41e9-8965-fc6e0f9f064a" />   
<img width="878" height="331" alt="image" src="https://github.com/user-attachments/assets/301b8a05-b19d-4428-b3fe-5834b6fca42b" />  
Here are the results comparing tests 1 and 2.  
<img width="1095" height="521" alt="image" src="https://github.com/user-attachments/assets/199969c6-c913-4db5-aeda-e9cdbe556f30" />  
<img width="1088" height="529" alt="image" src="https://github.com/user-attachments/assets/2b071424-806c-47d5-91d3-fdf30c9a7fe2" />  
They converged immediately again which is convenient. They had a 1.30 percent convergence so I rand the numbers on my safety factors and moved on to making a change.  
<img width="777" height="204" alt="image" src="https://github.com/user-attachments/assets/a1435f9d-f146-4107-bd47-e7a1612bf102" />  
<img width="803" height="419" alt="image" src="https://github.com/user-attachments/assets/9f19652c-b665-438e-88e3-7658467992cd" />  
## Inner loop 2
I increased the thickness to 0.3 inches and did a 0.02 in rounding on the insides of the holes to see if I could get rid of stress concentrations.  
<img width="492" height="762" alt="image" src="https://github.com/user-attachments/assets/95b62dd6-65da-4250-b9ff-95b961284747" />  
I again started with 1 in elements and 0.5 in elements for the first two tests. Giving me 1526 elements and 2323 elements. Here are the results for comparing tests 1 and 2.  
<img width="933" height="456" alt="image" src="https://github.com/user-attachments/assets/5460341b-d35c-4438-bd56-72d33fc567cb" />  
<img width="934" height="453" alt="image" src="https://github.com/user-attachments/assets/bb264ad3-bd3d-4e27-b778-b2ef247e9fb5" />  
I calculated the convergence as 29.6 percent so I would need to refine the mesh.  
<img width="677" height="179" alt="image" src="https://github.com/user-attachments/assets/2d8deee4-b41e-4a5b-9fb6-f43f0d11a566" />  
0.25 in elements gave me 9411 elements total. Here are the results for comparing tests 2 and 3.  
<img width="930" height="455" alt="image" src="https://github.com/user-attachments/assets/3d787b26-0e1a-4d11-983a-8ee1d325e048" />  
<img width="937" height="449" alt="image" src="https://github.com/user-attachments/assets/e17d5063-2bf7-4e5d-b919-59678d202d81" />  
I calculated convergence to be 31.6 percent so I would need to refine the mesh.  
<img width="657" height="171" alt="image" src="https://github.com/user-attachments/assets/c6394da5-b28d-473e-ad11-d31272c71ec7" />  
I increased it to 0.2 in elements and I got 56814 elements. Here are the results comparing tests 3 and 4.  
<img width="936" height="454" alt="image" src="https://github.com/user-attachments/assets/93f8302c-5f09-4cc0-9efb-a84365af7780" />  
<img width="932" height="444" alt="image" src="https://github.com/user-attachments/assets/84de8207-50c8-4bf4-ac66-53a6ab195ef9" />  
I calculated convergence and got 14.5 percent. So the results never converged and I moved onto calculating my safety factors and other things for the table.  
<img width="668" height="351" alt="image" src="https://github.com/user-attachments/assets/8662b616-6577-4221-9b8a-145e593fcaa9" />  
## Inner loop 3  
I increased the thickness again and increased the rounding on the holes to try one last time to move the stress away from the edge of the upper hole.  
<img width="675" height="739" alt="image" src="https://github.com/user-attachments/assets/2ce807c8-721d-480f-9522-9b7572064174" />  
I again started with 1 in elements and 0.5 in elements for the first two tests. Giving me 1305 elements and 2736 elements. Here are the results for comparing tests 1 and 2.  
<img width="927" height="449" alt="image" src="https://github.com/user-attachments/assets/99270061-548d-462d-b03e-78bfb89c9367" />  
<img width="933" height="448" alt="image" src="https://github.com/user-attachments/assets/4051481d-1c8e-4134-bc19-3b2fd030fc41" />  
The results converged immediately with 0.29 percent. So I calculated the safety factors and put all my values into my table.  
<img width="679" height="170" alt="image" src="https://github.com/user-attachments/assets/0b3d07b3-2d68-4e06-a851-031ef253372c" />  
<img width="680" height="359" alt="image" src="https://github.com/user-attachments/assets/5c961dfc-a4a7-425e-aefd-83a95745908e" />  
## End of outer loop  
I was able to decrease the amount of stress experienced in the material and reduce the dislocation. Overall I would say my changed weren't incredibly significant but it was very simple geometry and I was focusing my mental energy on looping through the process. I was able to increase the safety factors heavily and I would say I still improved the design using the FEA method.  
<img width="885" height="447" alt="image" src="https://github.com/user-attachments/assets/17cd0de2-7e99-4b54-8a5e-656f45e0ace0" />  
## Reflection  
During this assignment I spent a lot of time at the beginning just learning how to do this method inside the program of Creo. It wasn't super complicated and I think it was more detailed than the way Solidworks does it. This whole process combined things that I learned in class with a practical application for them to used. I was able to analyze a structure and see where it was weakest then formulate and implement an idea to improve the design. Then being able to test my idea and iterate on it was very fulfilling to do. Seeing the results improve across iterations made me feel productive and demonstrated my ability to reengineer and idea in a feedback loop. I also learned how meshes work. The computer is given a set of parameters and then distributes the body into elements and solves equations on every one of those lines between them. Finer meshes means more equations which means theoretically better results. In many cases the results can swing wildly and so doing multiple tests to see if I can get the data to "agree" or converge helps validate the final data points. Finer meshes also take longer to solve which wasn't much of a hinderance for me personally but I could easily see how if you had a larger part and you wanted to use a fine mesh, the analysis could get out of hand. I learned a lot of small things during this assignment that all culminated to give me a better understanding of the FEA method and it's place in the engineering process. I spent about 9 hours droning through this assignment.  
## Downloads  
<a href="../../files/a7bracket3.prt.1" download>  
    Download Final Bracket Design
</a>  
<a href="../../files/a7link3.prt.1" download>  
    Download Final Link Design
</a>  


