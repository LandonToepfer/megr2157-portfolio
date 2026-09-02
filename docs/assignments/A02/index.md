# A2 – Truss Stress Analysis

## Objective
In this assignment I was tasked with designing a truss within the given problem. The following image was provided with a set of givens.  
<img width="317" height="215" alt="download" src="https://github.com/user-attachments/assets/da5c4af9-7266-45b9-a400-f1fed7efbedf" />  
Figure #1.) The force and geometric constraints of the truss design problem.  
Choose a P between 20 - 30 kN. a = .4 m, b = .3 m. Point A is a pin and point B is a roller. Design a light weight planar truss using A500 structural steel. The cross sectional areas of each element is to be identical. The pins are to be identical to each other and each element has to have the same cross sectional geometry.  
## Analyze  
With the given situation my first step was to take in the knowns and unknowns and come up with a design. I started by pasting the givens into a document and writing out what I have to start with as this is always needed at the start of a project like this. Also having it all on the same document means I can go back and reference it without changing tabs and rereading the assignment. I also chose to have P = 20 kN as this just felt like my numbers would look slightly better but its a blind choice anyway as I had no foresight into the math. The following image is what I started with at the top of my document.
<img width="916" height="508" alt="image" src="https://github.com/user-attachments/assets/30df7090-9618-48a5-ab2a-dddd3f0c752c" />  
## Decide  
Moving into the first step, I had to draw out my design, calculate the length of my truss members, and solve symbolically then numerically for the internal/external forces. Starting out with drawing my design, I made the decisions to have a symmetrical design with two main triangle structures. I made the design symmetrical because intuitively I could see the math being symmetrical if the design was too. When drawing out my design initially I mislabeled the b value as 0.6 which I continued to run with for the remainder of the project up until I started my CAD which is when I noticed it. When I did I had to redo all my numbers which luckily only took 20 mins because I had all my equations and work shown. This was a major time loss. All numbers shown in images are correct and represent my final product. In the following image you will see my initial design, the truss lengths, and my rough judgement of which members will be in either tension or compression.  
<img width="860" height="613" alt="image" src="https://github.com/user-attachments/assets/fe8f8ff5-6097-487d-bb5e-e12a8cd0396b" />  
## Communicate
Next, I made a clearly labeled free body diagram of the design so I can reference which members are which and which joints are pins or not.  
<img width="1084" height="535" alt="image" src="https://github.com/user-attachments/assets/ac14558b-26d9-47a5-8ade-c0a173fa46da" />  
Then, I had to solve for the internal forces symbolically. This page was superbly helpful for the next step of solving numerically because I would end up using all of these equations anyhow. I was using the three static equilibrium equations. Sum of forces in the y, sum of force in the x, and sum of moments about a point. I did this for every joint until I had every equation I would need.  
<img width="831" height="822" alt="image" src="https://github.com/user-attachments/assets/396b2cf2-2556-4bd1-a260-93bdfce4253a" />  
I moved on to my fourth step which is solving numerically. Here you will see how I used the equations found previously plus a little trig to find all the forces needed. I started with pin A which found me AD and AE. I moved to pin D which found me DE. I flipped to the other side and did roller B which found me BE and BC. Then I moved down again to pin C which helped me find CE. This has all the final values in red and all the component values in blue so for my reference and yours, so that we can tell what is more important and find the values in the future easier.  
<img width="628" height="888" alt="image" src="https://github.com/user-attachments/assets/1d1250a8-23ad-4ee0-b37c-23fec1128953" />  
Now I had to find the cross sectional area of all my truss members which is my fifth step. This is done by using the largest internal force. Dividing the largest force by the yield strength of the given material gives me the area needed. Once I had the area needed I still had to multiply by the assigned safety factor of 3.5. The assignment also wanted me to find the approximate weight of all the members combined. So I used the total length of every member, and the cross sectional area to find the volume. Multiplying this by the density gave me the weight. This is where my second previously mentioned mistake came in and I had to redo the length, volume and weight. In this next image you will see all of that written out and executed. Keep in mind I am still showing you the correct values and not my mistake as this is a live document that I went back and changed.  
<img width="866" height="1223" alt="image" src="https://github.com/user-attachments/assets/01789b55-e4fb-48b0-8143-15be0f3cac3c" />  
Now I had to work on the pins themselves. I called this my step 6 and I needed to find a few things: the cross sectional area of the pins, and the weight of the pins. This was useful when moving on to finalizing the design in my CAD software. I listed my knowns and unknowns which helped organize my thoughts and narrow my initial goal. I needed to find the pin with the greatest forces which is along with the same logic as finding the member with the greatest forces. This is so all the pins can resist the loads and so that I make my design around the weakest link. I figured either of the bottom pins: C and D. This is because they are closest to the load P and experienced the greatest forces numerically. I drew a free body diagram of pin D because it was in tension and not compression so it was easier to think through but both pins are essentially the same. Pin D has three forces, but I knew the x components on the top would cancel so I combined those forces into one force in order for me to calculate shear force easier. With two forces on either side equal to 20kN, I used that as my shear force. The shear yield strength of the material is equal to the force over the area. I rearranged the equation to solve for area and started plugging numbers in as shown. Just like last time though there needed to be a safety factor which was 4 this time. Once I got my area I needed to do a few things with it, like find my volume and weight of my pins. I found my weight per pin and total weight of all five. Below you'll see this all in action.  
<img width="630" height="891" alt="image" src="https://github.com/user-attachments/assets/fea76994-77e5-41f6-9533-971d7df4ca60" />  
I now needed to start working in CAD, this would be my step 7. I started with a sketch of the initial problem to measure out where all my joints would be. I made sure my units were in millimeters because that is the unit I have to use for the truss thickness as well.  
<img width="1244" height="541" alt="image" src="https://github.com/user-attachments/assets/54521369-78b8-40da-8e34-3b477e3cfebe" />  
I then drew in the lines of all my truss members, which made me very happy to see the design in perfect proportions.  
<img width="1244" height="515" alt="image" src="https://github.com/user-attachments/assets/2610cb55-c7a6-4d29-b3f2-a9ffec58b5df" />  
I had to maintain the thickness of metal even at the joints so using math you can see at the bottom of step 6, I found the diameter of the circular joints. Where I could have the same thickness of metal and still have a hole in the middle for the pin. This ends up being 24.3 millimeters. Once I found this diameter, I drew in all the circles for these joints.  
<img width="1243" height="431" alt="image" src="https://github.com/user-attachments/assets/406a091a-e0ec-4cc5-8ea7-61369c488e3b" />  
Next, I needed to draw the truss with the correct thickness but I only had a centerline. This is where I had to make a sketch into a real object. I used the centerline to make perfect perpendicular lines off the joint with half the end thickness of the truss member which is 7.49 millimeters. I did this on both ends of the member and then connected the points I created to get the full shape. I repeated this for every member.  
<img width="933" height="675" alt="image" src="https://github.com/user-attachments/assets/d2cea16f-0ed7-4062-87eb-f228136a8d25" />  
Now with the sketch complete, I have all the points I need to start the extrusion process. This is how it was looking.  
<img width="930" height="338" alt="image" src="https://github.com/user-attachments/assets/6e8edce7-f0d8-4803-8663-a48590bf79ef" />  
I needed to clearly define the area that I needed to extrude so I had to put another sketch on top and trace the outline of the structure. The image below is how that looks, where the blue lines are my previous sketch, and the yellow lines are my new sketch. The program allows me to use the old sketch as solid points to draw from by generating points anywhere two lines cross.  
<img width="928" height="529" alt="image" src="https://github.com/user-attachments/assets/54540998-1e0e-4a4c-9655-ed05a830d7c9" />  
Now here is the completed area highlighted in purple before extrusion.  
<img width="930" height="325" alt="image" src="https://github.com/user-attachments/assets/efe03c17-a1fd-4952-a21b-0216bd0f27a7" />  
Now, I extruded it the same thickness calculated earlier.  
<img width="929" height="413" alt="image" src="https://github.com/user-attachments/assets/420b64d7-bc44-443b-b3e7-eb4987956c30" />  
I moved on to making the pin part which was a simple two step process. I made a circle with the calculated diameter.  
<img width="924" height="722" alt="image" src="https://github.com/user-attachments/assets/7ac50dab-df99-4831-9668-3b62d871f4f7" />  
Then I extruded the same thickness of the truss.  
<img width="929" height="684" alt="image" src="https://github.com/user-attachments/assets/a4dc5072-eba7-4b3a-9f40-5c7820ca17b8" />  
Before assembly, I needed to make holes in the truss for the pins to live in.  
<img width="928" height="765" alt="image" src="https://github.com/user-attachments/assets/88a50122-1373-43bf-abd6-89c4f65f92db" />  
This is how the finalized truss looks.  
<img width="930" height="274" alt="image" src="https://github.com/user-attachments/assets/d01d5782-975f-4ab9-be58-456bfca179cc" />  
Here is how it looks after the pins are in it and its assembled.  
<img width="1299" height="407" alt="image" src="https://github.com/user-attachments/assets/8d4505dc-a107-4161-a6cb-11f9d8e23cf6" />  
Now I had to calculate the mass of the truss using the CAD program. I entered in the material densities and assigned them to truss and pins. Then I ran the mass properties calculation and I got the total mass to be 5.132 kilograms.  
<img width="597" height="835" alt="image" src="https://github.com/user-attachments/assets/deb49f4b-4ae3-4bd0-85b6-899ff2623f98" />  
Over the course of the project I learned how to take an idea and turn it into a complete design. I took concepts learned in the classroom to calculate dimensions and forces. Those concepts actually had an end goal now, I didn't just need to find the answer, I needed the answer to decide how thick my beams needed to be. This whole project turned conceptual into practical. I was able to use static equilibrium equations to calculate internal loads. I was able to use solid mechanics to calculate the cross sectional area of the pins. I also used to find the cross sectional area of the beams needed to resist the strongest force. I learned what safety factors are and where to use them in the math in order to ensure adequate strength to match design requirements. Lastly, I found out how to check the mass of an assembly in my CAD program by assigning densities to materials which I had never done before.  
Overall, this project took me about 10 hours of pondering, calculating and executing. A lot of my time spent was just understanding what to do and how the assignment wants me to do it. The instructions were a little vague, specifically around the CAD portion on whether I needed to make every single member a separate part or just one solid structure which is what it said at the very bottom of the document next to the example. So I went with what the example displayed. A lot of my effort in this project went into looking at the examples and instructions together to get a better understanding of where I needed to go as an individual.
# Likelihood of Failure Modes in Truss Components  

## Part 1 - Truss Members  
I did research to get a general understand of different failure modes of members. There are three main failures, yielding, fracturing and buckling. Yielding and fracturing are generally for members in tension. Whether it yields or fractures depends on the material properties of member. If the material is more brittle then it will fracture before it bends significantly. If the material is highly ductile then it might not be really strong but it will deform and stretch way before it fractures. The material used for this project is A500 structural steel which is generally considered ductile because most carbon based steels are.  
Now considering the truss material is considered a more ductile metal, I would predict that it would fail through yielding and buckling than through fracture. Now the truss member was designed to handle the loads specified in the challenge. If I had to assign the most likely failure modes for each member than I would assign yielding to my tension members and buckling to my compression members. The reason I would say buckling to my compression members is because of the length of the beams. Compression yielding is more likely in shorter beams, but these are much longer compared to their length. My compression members are 2, 3 and 4. My tension members are 1, 5 and 6. One thing I did notice while doing the previous work is that structural steel seems to be shaped and hollow, like a hollow square or circle. If I had to make one change to the design of my truss I would probably do what they do in real life and make it a hollow square with some calculated thickness.   
## Part 2 - Pin Connections  
From what I was able to gleam from a paper on pin failures they seem to have been categorized but are all a combination of either the pin breaking, the plate breaking, or a little of both. From the scope of this project, I don't think I could predict which exactly would happen with math but I could take an educated guess. I would assume that our method of failure would have to do with the metal of the joint bending before the pin itself bends. This is because of the safety factors used to design the pin vs. the members. The safety factor of the pin was 4 while the truss member area was 3.5. Also, because we know that the steel is ductile, its more likely that it would bend than crack. This might result in a failure mode called "Dishing". This is where the plates or "lugs" start to deform out of plane and buckle for the pin to slip out.  

## Sources For Second Portion of Assignment  
https://www.youtube.com/watch?v=KKGMr6BDSlQ  
https://www.youtube.com/watch?v=vlZaPx-7JrQ  
https://oa.upm.es/85661/3/85661.pdf  













