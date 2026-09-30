# A6 – Bracket Drawing

## Objective
During this assignment I was tasked with creating a drawing of the bracket designed in the previous assignment. I had to start by creating a CAD file though. I had to use parametric design to create the bracket by using equations to dictate the final dimensions. I did this in Creo Parametric by using its parameters and relations tools. I started by defining all of my global variables that I would need to use across the part. All of these variables cannot be defined by equations so they have to stay constant. This is what the tab of my parameters tool is looking like at the start of this process.  
<img width="839" height="551" alt="image" src="https://github.com/user-attachments/assets/fb6981f2-3cb5-4ecd-b05a-607c3874cd03" />  
I then started with feature A just like when I designed it. From the last assignment this feature has a greater dimension requirement for stiffness so I used that equation for the radius.  
<img width="1235" height="689" alt="image" src="https://github.com/user-attachments/assets/3c174d90-e6d3-4f37-8d28-7d794325621d" />  
I then went and extruded it and set the length of it to my constant, length A, which is 6 inches.  
<img width="1131" height="550" alt="image" src="https://github.com/user-attachments/assets/2d875128-7cb6-4726-b639-4b1b43ae8651" />  
I also defined my radius used in my part level relations so it can be referenced in other features.  
<img width="1127" height="632" alt="image" src="https://github.com/user-attachments/assets/e7dbab0b-9944-4343-89b7-7aff553db6e9" />  
I then went ahead and defined the sketch for feature B and used the equation dictated by stiffness again for this feature. I did this on the inner level or feature level of my relations tool, just like in feature A.  
<img width="1180" height="622" alt="image" src="https://github.com/user-attachments/assets/5755601e-1f5d-47c6-8031-3c7f16742810" />  
I then went and defined this thickness in part level relations to be used later.  
<img width="1198" height="523" alt="image" src="https://github.com/user-attachments/assets/0794dfab-1635-4613-b88e-bc541269a46a" />  
Then I extruded feature B the known about of length which I chose as 4 inches.  
<img width="1146" height="582" alt="image" src="https://github.com/user-attachments/assets/bc0ee4ce-fec5-4c06-9cb4-cdcfcc6ed3ad" />  
I then started with the cross section of feature C. I defined the height of it using the equation dictated by strength for this feature because I had a larger dimensional requirement. I also was able to define its width using the dimensions and tolerances given by the T-beam it is connected to as well as the fit clearances found in the previous assignment.  
<img width="1100" height="496" alt="image" src="https://github.com/user-attachments/assets/59a424a8-7078-45bc-ba26-25b4ab1729b2" />  
I then moved into feature D. The height was defined the the beam dimensions and the fit clearances. The width was defined by using a strength dictated equation as it had the larger dimensional requirement for this feature.  
<img width="1231" height="579" alt="image" src="https://github.com/user-attachments/assets/a0bc863b-d1ff-49b6-b234-4301b34eb744" />  
I then moved into feature E. The width was defined the the beam dimensions and the fit clearances. The height was defined by using a strength dictated equation as it had the larger dimensional requirement for this feature.  
<img width="1075" height="720" alt="image" src="https://github.com/user-attachments/assets/b1715b26-ea9b-447b-bc6b-4e9ba3bdb1cc" />  
I then went and made equal shapes on the other side that essentially just mirror it using equal constraints.  
<img width="909" height="667" alt="image" src="https://github.com/user-attachments/assets/4ef5179d-d309-4ab6-85aa-d1b4c01927e0" />  
I went and extruded features, C, D, and E. This was using the same length of A which I already had a variable of.  
<img width="1223" height="662" alt="image" src="https://github.com/user-attachments/assets/a9f3223f-744c-4927-9569-f05d9f99ed84" />  
I now needed to make a drawing out of this part which is quite easy as I've done it many times before. I went back to my previous assignment to gather the clearance tolerances for each fit as they are very critical and then was able to find the + and - tolerances. It's a standard third angle drawing and I added an isometric view which was personal choice and allows a better view of the part as a whole. I also had a name block format premade that was leftover from my previous CAD class. This allowed me to pop in a name block and finish the drawing.  
<img width="991" height="767" alt="image" src="https://github.com/user-attachments/assets/4c85bae3-cdca-4920-b6a3-378686466800" />
## Lessons Learned
I used equations to determine dimensions in Creo for the first time during this assignment. I found it rather confusing at first but it was surprisingly simple once I knew what was going on. I used a stiffness equation for the thickness of B for example. I did this by having global variables that any relation or dimension can reference in my parameters tab. These variables were things that were constant like my material's stiffness, the length of A, the force applied (F) and more. I then was able to use the relations tool to define a dimension. The relations tool was dependent on what portion of the part you were working on. There are some feature level relations that would define something like a sketch. Then there was the global level or part level relations that can pull from any feature and define any feature.  
I had two features on my drawing that had tolerances in the ten thousandths but it was only because that how the fits were defined in the machinery's handbook. A machinist might not be able to get down into the ten thousandths but for the purpose of the assignment I found it fitting to take that extra step of precision to define the full range of values for the features that had to have those specific fits. Besides that I made every other dimension that wasn't functional round to the third decimal place because any more was unnecessary, and any less precision would ruin the strength of the part because of the scale it is being designed at. Generally speaking though if every part designed at this scale had such tight tolerances of the third decimal place then it would be quite expensive to be able to ensure those tolerances stay true. This is because of the time and special machines that might be needed to achieve these feats.  
## Time Spent  
overall I think I spent around 8 hours on this assignment.  
## Link Drawing
I was tasked with making the link from the last assignment as well as a drawing of it. I started of by making the cross section of this link. I used all the dimensions from the last assignment. I used a 1 inch gap minimum around the holes and I defined the holes using a 1 inch hole for the one inch shaft and I used the diameter of feature A for the other hole as specified. I had to go back and readjust the sizes of these holes for tolerances of fits.  
<img width="513" height="649" alt="image" src="https://github.com/user-attachments/assets/e2007865-2817-4866-ab57-c3fc364d5715" />  
I then defined my known global variables and used them to parametrically design the thickness of the link.  
<img width="772" height="267" alt="image" src="https://github.com/user-attachments/assets/2ded84b7-0f64-49f1-a3e8-1e56f97be56f" />  
I used those global variables for an equation designed around strength for this link. I put that equation into the part level relations tool to define the thickness.  
<img width="1233" height="783" alt="image" src="https://github.com/user-attachments/assets/fe2824e9-37c1-48cf-a837-bac2746aa895" />  
I used the tolerances of the hole fits to readjust the dimensions of the holes. This then populated into the drawing and I added the tolerances needed to still fall into my fit classes.  
<img width="1439" height="1115" alt="image" src="https://github.com/user-attachments/assets/388cb9f2-fe90-4b03-9a86-525cbc977c99" />
I had the same process with the link drawing. It was fairly easy to create and I had a template for the name block that I used.
## Downloads  
<a href="../../files/a6bracket.drw.zip" download>  
    Download Bracket Drawing
</a>  
<a href="../../files/a6bracket.prt.1" download>  
    Download Bracket
</a>  
<a href="../../files/a6link.drw.zip" download>  
    Download Link Drawing
</a>  
<a href="../../files/a6link.prt.1" download>  
    Download Link
</a> 
