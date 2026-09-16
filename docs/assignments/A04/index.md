# A4 – Motor Mount

## Objective
In this assignment I was tasked with designing a plastic motor mount. The specific motor was given along with it's dimensions. I was given the option to choose one of three different plastics to make it out of. I chose ABS for no particular reason. Multiple assumptions were made as well. The weight of the motor was to be neglected. There was an applied force of 300N on the shaft of the motor that will be used for a moment later on. One side of the mount attaches to a rigid wall while the other attaches to the motor. We are to design the dimensions of the mount parametrically by designing for material strength and for allowable deflection. In this next image you will see how I listed my requirements and highlighted what I found important.  
<img width="2146" height="939" alt="image" src="https://github.com/user-attachments/assets/08c4449d-0b58-4f68-928d-806e798edcbf" />  
## Feature 1  
Moving on to the first feature, were starting with the portion connected to the motor. Here we have a few dimensions, the length (L), the width (h), and the thickness (b). I started with listing my knowns and unknowns, and drawing a diagram of how I have to design this part. My knowns are the material and it's properties, the safety factor, the applied force (P) and what that is as a moment (PL), how I'm supposed to design it (cantilever setup), and finally that the holes are accounted for in the safety factor. Now what I needed to do here was pick my length and width for my design based off of how big my motor was and then solve for the thickness using my different known properties. I picked h to be 32mm and L to be 34mm. Then I was able to solve for my thickness two separate ways. The first way was using a strength equation using the yield strength of the material. The second way was for deflection using the Young's modulus or stiffness of the material. After solving, I plugged in my numbers and found thickness for strength to be 3.74mm and thickness for deflection to be 6.75mm. Now we want both strength and stiffness so I chose the larger of both numbers so that it doesn't fail at either. Below you will see my work for the first feature. My numbers in blue is my work for strength and my numbers in green is my work for deflection.  
<img width="1308" height="1265" alt="image" src="https://github.com/user-attachments/assets/7f931c0d-4c35-4892-843e-b1b5a2fa245f" />  
## Feature 2  
Moving on to the second feature, the wall mounted portion. Starting with my knowns, again we know the material and it's properties, the safety factor, the applied force (P) and what that is as a moment (PL), and max deflection. A few new things to note are that are old thickness is going to be the same as our new thickness. I also need to choose a new length (L) for this feature. I actually played around a lot with my length after solving for my thickness both ways again in order for my thickness to be reasonable. I ended on my length being 30mm. The equations are the same exact equations from feature one however I stilled solved them and have all the same work. After plugging in my numbers I got 3.30mm for my strength thickness and 4.63mm for my deflection thickness. Now, its the same process of choosing the larger number so that the design can support both requirements. Note that the end of feature 2 is going to be attached to the side of feature 1. In the next image you will see my work for feature 2.  
<img width="912" height="905" alt="image" src="https://github.com/user-attachments/assets/225c5923-3151-4efa-a491-2c6635ebbba1" />  
## Isometric sketch  
The assignment wanted me to draw the part altogether on paper isometrically. I did this by finding isometric paper online so I can print it and then drawing the part to mostly accurate dimensions using the pattern of the paper. The drawing has all the dimensions of feature 1 and feature 2 while also including the holes and features needed for the attachment points.  
<img width="699" height="507" alt="image" src="https://github.com/user-attachments/assets/dcafd51f-2d4d-48b1-876a-d26b5ee6de75" />  
## CAD Model  
I started off designing the part in CAD with the same flow as I did during the earlier portions of this assignment. I started by sketching the area (Length and Width) of Feature 1.  
<img width="1011" height="741" alt="image" src="https://github.com/user-attachments/assets/a5be2f90-dadc-4603-82ae-52f0e4e53275" />  
I then extruded that with the thickness found for feature 1 that designs for deflection (6.75mm).  
<img width="1073" height="791" alt="image" src="https://github.com/user-attachments/assets/04d018f1-f57c-48f0-ab8d-bdb5bc40ba28" />  
I then extruded off the side of feature 1 to form feature 2. This attachment was also mentioned at the end of the feature 2 portion of this assignment. I used the parametric constraints to define the area from end to end so that I would have the same width (h). I then used the thickness found for feature 2 that designs for deflection (4.63mm).  
<img width="1103" height="605" alt="image" src="https://github.com/user-attachments/assets/467712f2-1791-4909-8180-e91d27470dc4" />  
Then I extruded this area using the length of feature 2. I hope that the green outline of where this feature starts helps you separate the two blocks.  
<img width="1109" height="489" alt="image" src="https://github.com/user-attachments/assets/80908959-4791-42fa-a925-cced36c947b1" />  
Now I needed to start putting the holes for the motor attachment into feature 1. I started by defining a central axis so that I could parametrically define the holes around it. I chose it's location to be half the width of the motor from the top end (right side) of the mount. Then I chose it to be in the middle of the horizontal dimension (top to bottom). This provided a perfect clearance for the motor and centers its location.  
<img width="1106" height="687" alt="image" src="https://github.com/user-attachments/assets/fbe85623-ee95-4dbd-aa44-9d6b7edfa188" />  
With that axis, placing the holes was really easy as I could define them coaxially. I started with the indented section that would help seat the extended portion of the motor head. These dimensions for the motor can be found in the very first image of the assignment and some are circled in yellow. This feature of the motor extends 2mm out and is 18mm in diameter. Here you can see that first hole.  
<img width="1116" height="817" alt="image" src="https://github.com/user-attachments/assets/b41b11ad-f53d-4685-b96a-cd01ca2137b3" />  
Then I made the hole for the motor's shaft. I placed the hole coaxially, set its width to 6mm which is the diameter of the shaft. I set the hole to go through the whole part.  
<img width="1114" height="896" alt="image" src="https://github.com/user-attachments/assets/3dc62694-5766-4b9a-9f74-74b217c5e849" />  
I now started on the clearance holes for the mounting holes. They were told to me to be 3.4mm in diameter. I defined the hole placement radially. I set it's radius to be 11mm which is half of the diameter listed on the part specs from hole to hole. On the part specs, there are matching holes on all 4 sides. I'm about to make all of those. I set the diameter of my hole to be 3.4mm and for it to go through the whole part. I also needed to choose a reference plane to define the angular axis so I chose the one you can see in the top of picture tinted with a light brown color.  
<img width="1110" height="851" alt="image" src="https://github.com/user-attachments/assets/35fb6273-0342-4ea2-ac7b-6a6cca7b9a45" />  
Now I'm going to use a pattern to duplicate the hole around the central axis. I used the angular dimension which is highlighted in green in the center of the picture. It was set to 0 degrees in this and the previous picture. Using the angular dimension I set the member count to be 4, as I want 4 holes in total. Then I set the increment to be 90 (in degrees). This will place the hole perfectly on each orthogonal corner. This pattern keeps the radius from the center the same and the diameter of each individual member the same.  
<img width="1120" height="774" alt="image" src="https://github.com/user-attachments/assets/0fe32cc6-e596-48aa-bc9d-de29930c30e8" />  
Now you can see how that pattern turned out with the four cloned hole features (Highlighted in green).  
<img width="1115" height="739" alt="image" src="https://github.com/user-attachments/assets/f373119f-fd7f-4781-8d2a-eac81edeb458" />  
I then moved onto feature 2 and its attachment to the wall. I wasn't given any specific dimensions on how the mounting holes were to be defined so I kept the same dimension as the mounting screws for the motor. I also chose the position to be 2 times the diameter of the hole from the top corners. I then calculated the distance between those two top holes in order to get that distance so that I can place 4 of those holes in a square. I defined the holes starting with one place 6.80mm from the corner. Then placed 3 more with a distance of 18.40mm which was the distance aforementioned.  
<img width="1114" height="591" alt="image" src="https://github.com/user-attachments/assets/6abcba2c-5443-4c4b-97bb-45a5614eb8f4" />  
Now here's how those holes turned out (Highlighted in green).  
<img width="1115" height="605" alt="image" src="https://github.com/user-attachments/assets/0faa94b2-eada-4d4e-afa4-8551e32c3f29" />  
Now here is the final design.  
<img width="862" height="939" alt="image" src="https://github.com/user-attachments/assets/6045de3d-41e4-483d-a01c-77588867b80b" />  
## CAD Drawing
I also had to make my part have a CAD drawing which was fairly easy as I did it in a previous course fairly often and had prebuilt formats saved. I placed all of my views with real and hidden lines being shown. These 4 views are front, top, right, and an isometric view. The first three views have all of my dimensions displayed so that someone would be able to build my part from just the drawing itself. Below is a picture of what it looks like in my CAD program.  
<img width="2547" height="1439" alt="image" src="https://github.com/user-attachments/assets/89fbe016-c7ca-4cf0-8bc7-03979f207e84" />  
Here is what it looks like exported as a PDF.  
<img width="1049" height="812" alt="image" src="https://github.com/user-attachments/assets/1f190e60-cb39-4d8b-a3f8-0203c10b6e26" />  
## Downloads  
<a href="../../files/a4motormount.prt.1" download>  
    Download My Part Here  
</a>  
<a href="../../files/a4motormountdrawing.zip" download>  
    Download My CAD Drawing Here  
</a>  
<a href="../../files/a4motormountdrawing.pdf" download>  
    Download My Drawing PDF Here  
</a>  











