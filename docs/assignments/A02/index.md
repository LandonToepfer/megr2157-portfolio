# A2 – Truss Stress Analysis

## Objective
In this assignment I was tasked with designing a truss within the given problem. The following image was provided with a set of givens.  
<img width="317" height="215" alt="download" src="https://github.com/user-attachments/assets/da5c4af9-7266-45b9-a400-f1fed7efbedf" />  
Figure #1.) The force and geometric constraints of the truss design problem.  
Choose a P between 20 - 30 kN. a = .4 m, b = .3 m. Point A is a pin and point B is a roller. Design a light weight planar truss using A500 structural steel. The cross sectional areas of each element is to be identical. The pins are to be identical to each other and each element has to have the same cross sectional geometry.  
## Analyze  
With the given situation my first step was to take in the knowns and unknowns and come up with a design. I started by pasting the givens into a document and writing out what I have to start with as this is always needed at the start of a project like this. Also having it all on the same document means I can go back and reference it without changing tabs and rereading the assignment. I also chose to have P = 20 kN as this just felt like my numbers would look slightly better but its a blind choice anyway as I had no foresight into the math. The following image is what I started with at the top of my document.
<img width="916" height="508" alt="image" src="https://github.com/user-attachments/assets/30df7090-9618-48a5-ab2a-dddd3f0c752c" />  
Moving into the first step, I had to draw out my design, calculate the length of my truss members, and solve symbolically then numerically for the internal/external forces. Starting out with drawing my design, I made a symmetrical design with two main triangle structures. I made the design symmetrical because intuitively I could see the math being symmetrical if the design was too. When drawing out my design initially I mislabeled the b value as 0.6 which I continued to run with for the remainder of the project up until I started my CAD which is when I noticed it. When I did I had to redo all my numbers which luckily only took 20 mins because I had all my equations and work shown. This was a major time loss. I also when recalculating the lengths at the very beginning, miscalculated again the lengths of my members 4 and 5 which I had to go back and fix again while writing this. All numbers shown in images are correct and represent my final product. In the following image you will see my initial design, the truss lengths, and my rough judgement of which members will be in either tension or compression.  
<img width="860" height="613" alt="image" src="https://github.com/user-attachments/assets/fe8f8ff5-6097-487d-bb5e-e12a8cd0396b" />  
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









## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

## Communicate

