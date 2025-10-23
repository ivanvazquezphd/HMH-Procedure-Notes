## Phase 1. Prescription

1. Go to `Quicklinks` > `Treatment Management` > `Prescribe Treatment`

2. Create a **new Course** by clicking on the drop down arrow ![[Pasted image 20250918105526.png]] and selecting `New`

![[Pasted image 20250918105510.png|center|250]]

3. Enter the course name, ex: C1a if first or C2a if second HDR treatment, and the intent

![[Pasted image 20250918105758.png|center|400]]

4. Select the `HDR Prostate Boost(Shared)`  if boost or `HDR Prostate\SV (Shared)` if monotherapy for your template ![[Pasted image 20251023105558.png|250]] 
	- This will populate the fields in the Treatment Prescription pane (ex: assign One Fraction)

![[Pasted image 20251023114000.png|center500]]

CT_HDR_Prostate 


FRaction name should be added.... 


## Contouring Stage

### 3. Open patient in contouring suit and update CT name

- **Confirm the diameter of the cylinder** by clicking on the `Distance` tool ![[{E4816867-BB8B-48AE-BD92-2775DEB6959C}.png]] and measuring the diameter of the cylinder. 
	- Round measurement to nearest known cylinder diameter (ex: 2.5 cm or 3 cm)

![[{ECC13B9A-0797-4CC0-AF09-9EFDAA6293CE}.png|center|200]]

- Change the name of the CT study to reflect the dimensions of the cylinder
	- Right click one of the icons representing the CT study, e.g., the `CT Image` icon on upper left corner > select `Properties`
- In the `ID` field, rename the image to "HDR_CYL_XXmm" or _(XX = diameter of cylinder in mm)_

![[Pasted image 20250815075539.png|center|512]]

>[!note] You may choose to name the CT with cm, e.g., `HDR CYL 2.0 cm` which some team members prefer. This is the same name we will use for the plan in a later step.
### 4. Add HDR cylinder contour set

In this step, you will add the contour set used for the course. The set of contours will be pulled from a clinical protocol as described below. There are two ways to obtain the set.

- **Option A:** 
	- Click on `Structure` from the top menu bar in the contouring UI
	- Click on `New Structures From Clinical Protocol` > `HDR CYL Dunn` > Click `Attach...` > Click `OK`
- **Option B:** 
	- Right click on the CT and select `New Structures From Clinical Protocol` from the drop-down.  
### 6. Start building the structure

- Click on a structure name to select it and begin contouring that structure
	- When you click on a structure, the drawing tools become active
- Use the shortcuts below to help you draw contours quickly