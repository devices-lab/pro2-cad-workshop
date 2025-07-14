# Electronics enclosure design walk-through with Onshape

![render](media/render.svg)

## Workshop activity

In this workshop, we’ll be demonstrating how to use computer-aided design (CAD) tools to design enclosures for electronics.
In Onshape, we’ve started designing a laser-cut enclosure for the solder:bit Gamepad with 3D printed spacers and button caps. You are given the task to design the rest of the enclosure insert and position the parts in the assembly to make sure everything fits.

### 1. Create a free Onshape account
Go to [onshape.com](https://www.onshape.com/en/) to create an account. This can be a student account that gives you unlimited private designs, or an account for makers where all your designs are public.

> [!NOTE]  
> It can be much easier to use a mouse rather than a trackpad for working in CAD, even if you brought your own laptop, consider using the lab computers for a better experience.

### 2.	Create a personal copy of the workspace 
Navigate to this [workspace](https://cad.onshape.com/documents/03e360eab7c280aec5a0fc8e/w/88428d9209ae85e1daa35f17/e/1467ba0b7f908cfe4e9b5ae8?renderMode=0&uiState=687371614301f30186208088) and make a copy to your own account from the hamburger menu in the top right. Take a look at all the design files in the bottom tabs containing part studios and assemblies. The Case Assembly tab is where we will mostly be working from. We’ve inserted a 3D model of the PCB from KiCad into this assembly and started designing parts around it.

![copying a workspace](media/workspace_copy.png)

<details>
<summary>TIP: Importing from KiCad</summary>

We've done this bit for you and have imported the board to start the design. However, if you're interested in doing this yourself, in KiCad, from the PCB Editor, go to File > Export > STEP / GLB ... , and select STEP as the format. You may need to set the board outline tolerance to "standard (0.01 mm) for it to recognise the boundary.

![Exporting Step files from KiCad](media/exporting_step.gif)

In Onshape this can then be imported with the plus icon in the bottom file tabs, Importing the step into a new part studio, then inserting the part studio into the assembly as rigid

![Importing Step files into Onshape](media/importing_step.gif)


</details>


### 3.	Understand the bottom panel design
Enter the Acrylic Case part studio in the bottom tabs. Here, within the context of the main Case Assembly, we’ve designed the bottom panel of the solder:bit case. In the left panel’s feature list, you can see the operations needed to make the back panel: we defined a plane below the bottom surface, we sketched out the outline of the panel,  then we extruded it to make it 3D. You can double click on any of these features to see how they were performed, or even change them. Your job is to replicate these steps for the top panel.

<details>
<summary>HINT: Can't see the PCB context?</summary>

If you don't see the context of the PCB, you may need to select it from the assembly contexts drop down in the top right.

![Seeing the context](media/context.png)


</details>

### 4.	Create a new plane
Using the Plane tool, create an offset plane 6mm from the top surface the PCB.

<details>
<summary>HINT: Creating an offset plane</summary>

![Creating a Plane](media/plane.gif)


</details>

### 5.	Start a sketch
On the plane we just created, start a sketch. Copy features from the PCB with the Use tool. Specifically, the outline, the 4 x 4mm mounting holes.

<details>
<summary>HINT: Sketching an using reference geometry</summary>

![Creating a sketch](media/sketch.gif)

If the context features aren't showing, make sure you've selected the right Assembly context in the top left dropdown.

</details>

### 6.	Close the cutout for the battery
Using the Line and Trim tool, fill in the cutout made for the battery cable.

<details>
<summary>HINT: Using trim</summary>

![using the trim tool](media/trim.gif)

</details>


### 7.	Create cut-outs for the buttons
With the Use tool, project the button positions into the sketch, then Create 6x 7mm circles on each of these positions for the button cut-outs

<details>
<summary>HINT: Using the buttons to draw centred circles</summary>

![using the circles tool](media/circles.gif)

</details>


### 8.	Create cutouts for the L and R buttons and the power switch.
After projecting features of the L and R buttons and power switch into the sketch, draw lines and rectangles make cutouts for these. You can use the dimensioning tools and constraints to make sure they are where you want them.

<details>
<summary>HINT: Creating cutouts for L,R and power</summary>

![making rectangles](media/fillets.gif)

</details>


### 9.	Clean up the edges and give the cut-outs a 3mm fillet.
With the Trim tool remove any extra edges that create bounded regions that we don't want to extrude. Then use the fillet tool to round off any corners with a 3mm fillet.

<details>
<summary>HINT: Using Trim and Fillet</summary>

![Using Trim and Fillets](media/fillets.gif)

</details>

Your sketch should look something like this now:
![sketch](media/sketch.png)

### 10.	Extrude the sketch
Complete the sketch with the green tick, and using the extrude tool, extrude the sketched region by 2mm

<details>
<summary>HINT: Using Extrude</summary>

![Using Extrude](media/extrude.gif)

</details>

### 11.	Insert the top panel into the assembly
Go back to the assembly and use the insert tool to place the top panel into the assembly. If you don’t specify a position it will automatically place itself in the position it was in the design context. Click the green tick to confirm. To constrain the part and keep it from moving when you drag it, use the group tool to group it with the already fixed bottom panel.

<details>
<summary>HINT: Using insert</summary>

![Using Insert](media/insert.gif)

</details>

We're done! Laser cutting files can be exported from the Part Studio. Right click on the surface and export the DXF or DWG for the specific face to cut out. You can also export STL, STEP, or 3MF files directly from the parts for 3d printing.

## Stretch Activities

### **Easy**: Placing button caps
If you have finished designing the top panel, consider placing button caps in the assembly. We've already designed these for you in the Button part studio. Use the Insert tool in the Case Assembly to locate the buttons and place them. Insert the buttons "as rigid" so that they remain combined when moving them about, and use the "Fastened mate" to fix them to the positions in the cut-outs.

###  **Medium**: Place screws and nuts
In the Assembly tab, use the Insert tool to insert parts from "Standard Context". Find an M4 x 16 Socket head screw and an M4 nut to go with it and place it in the assembly.


### **Hard**: Design your own button caps
Have a go at designing your own button caps in context. From the Assembly add a new Mate connector to one of the tops of the buttons. Click on the "Create new Part Studio in context" button on the right end of the toolbar. Select the new mate connector as the origin, and a new part studio should open with all the context of the assembly. Try sketching a profile of a button that you can use to make a solid of revolution with. By designing multiple parts, you can create buttons we can 3d print with different colours.

### **Expert**: Make it your own
Use the Onshape workspace as a starting ground to design your own additions to the solder:bit gamepad! E.g. A 3D printed accessory, a novel way to mount it or a way to make it more accessible. 

