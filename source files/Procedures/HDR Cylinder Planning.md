**Author(s):** Ivan Vazquez (based on notes by Parth Patel)
**Editor(s):** Forrest Ivey and Arjit Baghwala
## Preliminary Steps

### 1. Create the Treatment Prescription

- Go to: `Quicklinks` > `Prescribe treatment`

![[Pasted image 20250815110043.png|center|350]]

- Create a new treatment course if one doesn't already exists
	- Ensure you use the letter `a` at the end of the course, which indicates brachytherapy in our clinic
	
![[Pasted image 20250818001359.png|center|330]]

- Ensure that the template `HDR Cylinder (Shared)` is selected
 ![[Pasted image 20250818001736.png|center|500]]

- The template auto populates the fields.

![[Pasted image 20250815115033.png|center|400]]

- You should confirm the following values agree with what is expected for the patient:
	- **Fractions:** **3** If boost (using EBRT) or **5** for monotherapy (no EBRT)
	- **Total Prescribed Dose:** 3000.0 cGy
	- **Prescribed Dose/Frac:** 600.0 cGy
	- **Primary/Boost:** `Primary` or `Boost`
	- **Notes:** X.X cm diameter cylinder, 4cm treatment length
		- X.X is the size of the cylinder in cm, ex: 2.5 cm
	
> [!note] You can check the `Clinical Treatment Planning Note` to confirm the total prescription. 

![[Pasted image 20251008203827.png]]
### 2. Save as Draft

- Click on  `SAVE AS DRAFT` 
	- Note: You do not want to approve; Otherwise the physician might start moving forward with It

![[Pasted image 20250815145149.png|center|300]]
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

| Action                                         | Shortcut(s)                                           |
| ---------------------------------------------- | ----------------------------------------------------- |
| Reload all                                     | `Alt` + `F`, then `R`                                 |
| Switch contouring tools (cursor/pencil/brush)  | Right-click to highlight, then select                 |
| Window level adjustment                        | `Shift` + Move Mouse Cursor                           |
| Auto window level adjustment (reset contrast)  | `Alt` + `V`, then `A`                                 |
| Create new structure                           | `Alt` + `S`, then `Enter`                             |
| Fill structure info (when creating)            | `Down`, `Tab`, type name, `Enter`                     |
| Rotate through plane views                     | `Ctrl` + `R`                                          |
| Blend fusion image (CT/fused)                  | `Ctrl` + `A`                                          |
| Skip slices while scrolling CT                 | `Alt` + `Mouse Wheel`                                 |
| Delete contour on current slice                | Select Pencil Tool, then `Delete` key                 |
| Hide all contours except highlighted structure | Hold `H`                                              |
| Show/hide structure in adjacent slices         | `Alt` + `V`, then `S`, then `Enter`                   |
| Toggle between 2D/3D brush                     | `2`                                                   |
| Toggle between static/adaptive brush           | `A`                                                   |
| Use brush as eraser                            | Hold `Shift`                                          |
| Adjust brush diameter                          | Right-click and drag left/right                       |
| Cut/Copy/Paste contours                        | `Ctrl` + `C` (copy), move slice, `Ctrl` + `V` (paste) |
### 5. HDR Cylinder Contouring Guidelines

#### 5.1 General tips

- You should contour (at least) up to about ==**2 cm superior to the cylinder tip**==
	- Dose falls to negligible values beyond that and will, therefore, not contribute to our $D_\text{2cc}$ 
- Skip slices (ex: 2 or so) between your contours and make use of the `Interpolate Structure`
    - After interpolation, scroll through slices to inspect and adjust contours as necessary

![[Pasted image 20250814164550.png|center|450]]

![[Pasted image 20250814164742.png|center|450]]

  - **CT-Specific Tips:**
	- Use **abdominal windowing** to distinguish bowel wall from contents
	-  Don't be confused by air-fluid levels in bowel - contour the entire structure
	- Always check coronal and sagittal reconstructions to ensure anatomical continuity, especially for sigmoid
#### 5.2 Cylinder

- **Adaptive brush:** Use the **adaptive brush** and set the radius to a sufficiently large value so that the full cylinder cross section gets selected when you click on the cylinder.
- **Fixed radius brush:** Use a **circular brush with the same diameter as your cylinder** making adjustments near the dome and end where the cross sectional area change (decrease).
#### 5.3 Rectum

- **CT Identification:**
	- Appears as a tubular structure posterior to the vaginal cylinder
	- May contain air (dark/black) or soft tissue density (gray) depending on contents

- **Contouring Guidelines:**
	- **Inferior boundary:** Start at least 2 cm below the inferior extent of the active treatment length (4 cm from the tip of the cylinder)
	- **Superior boundary:** Continue to the rectosigmoid junction (where bowel begins to deviate laterally/anteriorly - usually around S2-S3 level)
	- **Key point:** Maintain a clear tissue plane between the rectal wall contour and the cylinder - they should not be touching
#### 5.4. Sigmoid Colon

- **CT Identification:**
	- Continuation of rectum that curves anteriorly and laterally (typically to the left)
	- May have a more "mobile" appearance compared to fixed rectum

- **Contouring Guidelines:**
	- **Transition point:** Begin where rectum starts to turn laterally/anteriorly (rectosigmoid junction)
	- **Superior extent:** Continue at least 2-3 cm above the cylinder tip to capture potential high-dose regions
- **CT appearance notes:**
    - May appear discontinuous on axial slices due to its curved/looping path
    - Include all visible sigmoid segments even if they appear "disconnected" on individual axial views
    - Use coronal/sagittal views to verify continuity
#### 5.5 Bowel Bag (Small Bowel/Remaining Bowel)

- **Definition:**
	- Peritoneal space containing small bowel and any other bowel loops not already contoured as sigmoid

- **Contouring Guidelines:**
	- **Superior boundary:** 2 cm above cylinder tip
	- **Inferior boundary:** Top edge of cylinder
	- **Lateral/anterior/posterior:** Follow peritoneal boundaries
	- **Exclude:** Muscle, bone, bladder, uterus (if present), major vessels, and already-contoured rectum/sigmoid

![[Pasted image 20250815162334.png|center|350]]

## Planning Stages using `Brachytherapy planning`

> [!info] This planning section is based on plan templates. For details on how to create a plan from scratch, see the notes near the end of this file
### 6. Open patient with course and CT image containing contours

- Open Objects ![[Pasted image 20250815182409.png]]> Highlight Patient > Select the relevant course ![[Pasted image 20250815182930.png]] > `Apply`
	- If not already done, you should name the course C1a 
		- The 1 here implies the first course of brachytherapy
- Open Objects ![[Pasted image 20250815182409.png]]> Highlight Patient > Expand `All Structure Sets` > Highlight `CT_1` > `Apply`
### 7. Insert a new clinical protocol reference

- Click on the course (ex: `C1a`) to select it and click **Insert > New Clinical Protocol Reference**. 
- Click `Next` and highlight `HDR CYL Dunn`. Click `Select`.
	- You need to check the box for *unapproved* protocols to see `HDR CYL Dunn`

![[Pasted image 20250817235628.png|center|624]]
### 8. Insert a new plan from template

- Click on the course (ex: `C1a`) to select it and click **Insert > New Plan from Template**
- A dialog box will pop up, showing the available RT prescriptions. Select the proper option (ex: `HDR Vaginal Cuff`) based on the name used in step 6 and click `Next >`
	

![[Pasted image 20250818002801.png|center|624]]

- For `Plan Template Selection`, ensure that both approved and unapproved templates are visible. Search for the `HDR CYL Xcm` option relevant to your case, where X is the diameter of the cylinder. 

![[Pasted image 20250818003840.png|center|624]]

- Select the correct target structure (ex: `Cylinder`) and click next

![[Pasted image 20250818004017.png|center|624]]

- When prompted for a primary reference point, ensure that the option for Cylinder is selected and click `Next >`.

![[Pasted image 20250818004047.png|center|624]]

- Review the dose parameters, ensuring that the dose per fraction and total dose match the expected value

![[Pasted image 20250818004106.png|center|624]]

> [!note] In some cases, the plan may not be associated with a clinical protocol. If this happens, double click the plan name (to open the properties) and select the relevant `Protocol Plan`

![[Pasted image 20250818170143.png|center|400]]




### 9. Align the cylinder template with the CT

> [!note] Completing step 8 creates a plan with a template of the cylinder. The template is initially positioned at the center of the CT scan, which generally doesn't match the expected position. Thus, you need to move the template into position 

- **Rotate the CT:** Orient the cylinder by rotating,  ![[Pasted image 20250818151916.png]], the sagittal and coronal planes so that the orthogonal plane markers run along the middle of the cylinder
	- Once done, the Cylinder should run vertically on the screen

![[Pasted image 20250818151449.png|center|450]]
- Click on the applicator to select it ![[Pasted image 20251009084344.png]] (you should see it become blue)
- Use the `Move applicator` ![[Pasted image 20251009084732.png]] and `Rotate applicator` ![[Pasted image 20251009084751.png]] buttons to align the applicator with the CT

![[Pasted image 20251009085722.png]]

### 10. Customize the `Dose` display

> [!note] The choice here can differ between physicists. Some physicists like to use three values (200%, 100%, and 50%) with colors of yellow, red, and blue, respectively. Other physicists prefer to use only two isodose levels (100% and 200%) with colors set to red and white, respectively. You may also encounter differences in preference between absolute and relative dose.

- **Option A:** Click on the elements on the top left corner of the axial plane to update the units and values (see Figure below)
	- Use yellow for 200%, red for 100%, and blue for 50%
	- Set the **Units** to absolute by clicking the `[%]` symbol so that it becomes `[cGy]` 

![[Pasted image 20251009091933.png|center|500]]


- **Option B:** Using the `Dose` icon to set relative dose and two levels
	- Right click `Dose` ![[Pasted image 20250818154725.png]]on the left panel and uncheck `Absolute Dose` *(If checked)*
	- Then, right click `Dose` again and click `Isodose Levels`
	- Keep only two isodose levels (100% and 200%) check-marked in 2D and 3D
	- Change their colors to red (100%) and white (200%). Then click `Apply` and `OK`

![[Pasted image 20251009092643.png|center|400]]

### 11. Defining `user origin` and  `default viewing plane` **and**
 
- Move the sagittal and coronal crosshairs  so that the sagittal and coronal planes run along the central axis of the cylinder
	- If your views are too clutter, turn off the Dose, Structures, etc.
- Once your sagittal and coronal planes are set, move the axial plane to *3mm (one slice) above the tip of the cylinder channel* (as shown in the top left on the figure) 
- Right click `User Origin` ![[Pasted image 20250818154029.png]] on the left panel and select `Set User Origin`
	- Under `Set to Predefined Target`, choose `Viewing Plane Intersections` > `Apply` > `OK`
	![[Pasted image 20250818154121.png|center|350]]
> [!note] You can now return CROSSHAIRS to this position in the default viewing planes by right clicking 'User Origin' and selecting 'Move Viewing Planes To User Origin' or simply double clicking the icon

- Click the `Set Default Viewing Planes` ![[Pasted image 20250818150617.png]] button followed by `Set to Current`, and finally `OK`
	- Now, whenever you hit `Reset Geometry` ![[Pasted image 20251009094202.png]] in the toolbar, you can quickly return to this ideal setup for planning

![[Pasted image 20250818150705.png|center|300]]

> [!tip] The physicians prefer if we select a position that displays the entirety of the dose distribution. For this, make sure you are zoomed out enough and the cylinder is high enough in the screen to display the full dose curves as shown in the image below.
> 

![[Pasted image 20251009093239.png]]
### 12. Add Clinical Goals for one fraction

- Ensure that the plan properties do not show a `Protocol Plan` and that the number of fractions is set to 1

 ![[Pasted image 20251009110721.png|center|300]]
- Click on `Planning` > `Add or Edit Clinical Goals ...`
- In the `Clinical Goal Templates`, find and select `HDR Cylinder Dunn_1Fx`

![[Pasted image 20251009110449.png|center]]

- Ensure your Clinical Goals are all green/passing. 
	- Right click top right window (usually reserved for 3D rendering) and select `Show Dose Volume Histogram View`. In the bottom panel that appears, go to the `Dose Statistics` tab. Check every OAR besides the body so that it displays on the DVH. Then, go to the `Plan Objectives` tab.

![[Pasted image 20251009111436.png|300|center]]

- Complete the Treatment Planning task:
	- **Option A:** Navigate to `QuickLinks`> `EMR` > `Care Path` > Right click on the relevant task and change the status to `Completed`
	-  **Option B:** Check the Tasks and Appointments in Aria for Physics-Brachy and change the status to `Completed`
- Now we simply wait for the physician to approve/modify our plan
	
![[Pasted image 20251009112931.png]]
## Mobius Secondary Calculation

### 13. Place Reference Point For Mobius

- (If not at the User Origin) Double click on the `User Origin` item ![[Pasted image 20250819121858.png]]
- On a coronal slice, align the sagittal crosshairs with the edge of the cylinder and, using the `Measure Distance` tool ![[Pasted image 20250819122127.png]] from the toolbar, measure **2 cm** down the cylinder channel from your user origin placement.
 - Move your crosshairs to the **surface** of the cylinder aligning to this distance (i.e., 2cm down from tip of cylinder, then move to surface).
 - Right click `Reference Points` in the left panel and select `New Reference Point And Location` and click anywhere on the images on the right. 
 - Name the point `Mobius` and set the type to `Target`. Then click `OK`.
 - On the coronal plane, move the horizontal (axial) and vertical (sagittal) plane indicator so that it intersects the side of the cylinder. 
 - Right click `Mobius` that appeared in the left panel after creating the Reference Point. Select `Move Reference Point To Viewing Planes Intersection`, which should place the marker on the cylinder surface 2cm down from tip.

![[Pasted image 20250818172504.png|center|600]]

### 14. Export your plan to the Mobius server

>[!warning] Ensure that the number of fractions is set to 1 before exporting the plan to Mobius for the check calculation. Also, you will need an account for the server to view the results. The exact recommended server might be different than the one in this notes. Check with senior members

-  Right click on the plan name (e.g., HDR_CYL_3cm) and select `Export` > `Mobius3D - Server 3`
- On the window that opens up, click the right blue arrow ![[Pasted image 20250820085811.png]]  (left corner) > `Authorize` (on pops up)
	- If the plan is not approved, you will get a warning. Ensure that all transfers worked by checking that all files 

![[Pasted image 20250820090056.png|center|600]]

![[Pasted image 20250820093045.png|center|200]]

-  Mobius will start calculating secondary dose immediately after sending the plan to it
## Post-Planning Documentation

### 15.  Retrieve PDF file from second calculation

- Go to the relevant Mobius Server using IP address below. Log in using credentials

| Server Name         | IP Address     |
| ------------------- | -------------- |
| Mobius Server 1     | `10.177.8.43`  |
| Mobius Server 2     | `10.177.8.70`  |
| **Mobius Server 3** | `10.110.16.21` |
- Click on the name of your patient on the list. Then click `Open PDF Report` *(Third icon from left)*

![[Pasted image 20250820093441.png|center|500]]

![[Pasted image 20250820093516.png|center|500]]

- Scroll to the bottom of the plan data & verify the percent difference shows a green checkmark *(i.e., Mobius 2nd Check & Eclipse Agree Within Tolerance)*.
- Save the report to the `P-drive` as `4-mobius`

```
P:\1. Methodist Dunn\3B. HDR Bravos Dunn\1. HDR Patient QA
```

- Go back to the plan in Eclipse. **DELETE** the `Mobius` reference point you created *(Only needed for second calc doc; Will make other docs/screenshots neater)*
### 16. Eclipse Plan Report

> [!warning] The number of fractions in the `plan properties` must be set back to the full amount of fractions (3 or 5) for this documentation for steps 15 - 17

- With plan still open, save the *Eclipse* plan report via: File > Print > Report > (Select 'Adobe PDF' In Name Field) > (Select `BrachyFull.tml` In Layout Field) > Click `Ok` > (Select the relevant patient path) > (Name the PDF file as `1-report`)

![[Pasted image 20250820114751.png|center|400]]
### 17. DVH Plan Report

- With the plan DVH still displaying in the top right, go to `Dose Statistics` tab on the bottom panel and check in *all structures* so they show on DVH
- Click on DVH panel in top right. Then, (Right Click) > Print DVH Report > (Click 'Ok') > (same path as other files) > (Name the file `3-dvh`)
### 18. Screenshot of Orthogonal Views

-  Double click `User Origin` in the left panel. 
- Click `Clinical Goals` tab in bottom panel > Click `Clinical Goals` to display protocol structure DVH should still be displaying on the right panel.
- With the window showing the Clinical Goals at the center, click on `File` > `Print` > `Screen`
	- Change the page orientation to `Landscape` by clicking on `Properties` > `Layout` and changing the Orientation to `Landscape`
- Save the resulting file in the same folder as the previous file using the name `2-iso`
### 19. Combine the documents into one PDF file

- Select all of the files > `right click` on either one > select `Combine files in Acrobat`

![[Pasted image 20250820144114.png|center|300]]

### 20. Adding an imaging course

- Navigate to `QuickLinks` > `Treatment Planning` >` External Beam Planning`
- Click on `Inset` > `New Course...`
- Name the Course `C1a-Imaging` (or `C2a-Imaging` if second course of brachytherapy and so on...)
- Click `Insert` > `New Plan from Template...` > `DunnBravosSU` > `Next >` 
- Select the `C1a-Imaging` course from the Available courses > Click `Next >`
- Select `Omega` as treatment unit > Click `Next >` (Do not change the Dose...just click `Next >`)
- When prompted, you can leave the Cylinder as the target or check the `No plan target` box
- Select the `User Origin` as the primary reference point > Click `Next >`
- In the Isocenter placement for all fields dropdown, select `At image origin` > Click` Next >`
- Ensure the patient position is `Head First-Supine`
- Right click the DRR icon > `Edit DRR` > Select `Abdomen.dps` > check `Apply to all fields` > `Apply`
![[Pasted image 20251010153418.png|center|500]]

- Navigate to `QuickLinks` >  `Treatment Management` > `Treatment Preparation`
- For the tolerance table (Tol. Table), select a `Non-Index`
- Set the `Imager Vrt` to `50.0 cm`

![[Pasted image 20251010164917.png|center|650]]

### 21. Set the dose limits

- Return to `Quicklinks` > `Treatment Planning` > `Brachytherapy Planning`
- Double-click your reference point (`Cylinder`, `CTV`, etc) on the left panel. 
- In the `Dose Limits` section of the `General Tab`, enter the following:
	- **Total**: (No. of Fxs x 600cGy) 
		- Total Dose Allowed For FULL COURSE
	- **Daily Dose Limit**: 600cGy 
		- Dose allowed to patient per day
			- Note: This value can Be 1200 cGy If the patient has 2 Treatments 6 Hours apart in a Day, ex: 'BID' Regime
	- **Session Dose Limit**: 600cGy
		- Dose allowed in a single treatment session or fraction
- Then, hit `Apply` and `OK`

![[Pasted image 20250820171733.png|center|400]]

> [!note] This step is necessary to allow us to plan-approve our plan (next step); Without it, a warning would appear for planning approval regarding inability to monitor plan dosimetry (e.g., reference point serves as a dose 'accumulator' to track the fractions given.
### 22. Approve the plans

- Approve the HDR plan:
	- Right click your plan in the left panel and go to `Plan Approval` > `Planning Approved` 
	- Acknowledge any minor warnings (ex: unapproved or rejected structures) and approve. 
	- Provide login credentials as the final verification. 
		- A blue box appearing around your plan means it was **PLANNING** approved (because it was just done). Later, a green box around the plan will mean it was **TREATMENT** approved.
- Approve the imaging course:
	- Right click the `DunnBravosSU plan` > `Plan Approval` > `Planning Approved` > `NExt >`
	- Select the box saying `Continue planning approval without calculating dose and/or MUs`
	- Continue until prompted to input your password
## Adding Documents to Aria

### 23. Access documents

- With the patient still open, go to **Quicklinks > Documents**.
- Click `Import` on the top bar (NOT "New" On The Top Left). 
- Go to the file with your combined documents in the patient folder and select it.
- Once the document is pulled up, edit the following details at the top under 'Patient Document Details':
	- **Authored By**: (Look Yourself Up)
	- **Supervised By**: Dr. Farach (Or Treating Physician)
	- **Document Type**: **Treatment Plan - Initial** _(All Fractions Receiving An Individual Plan Are Specified With This For Billing Purposes; HDR Cylinder's First & Only Plan Is Specified This Way; Then With **Treatment Plan - Decay Calc** For All Subsequent Fractions Decay-Calculated With The Original Plan)_
	- **Template Name**: `HDR Cylinder`

> [!warning] UNCHECK 'COMPLETED' ON TOP RIGHT!! Otherwise Physician May Sign Off BEFORE Physics Approves

- Once finished, hit `Ok`(**NOT `Sign Off`**)_.

---
## Additional Documents

> [!warning] ONLY perform the steps below if this is the first time planning for the patient
### 24. 'HDR Vaginal Cylinder Consult' document

- Go to **Quicklinks > Documents**.
- Hit `New` in the top left corner. Then, click `Template` in the bottom left of the embedded Word document that appears. Check `Show All Templates`
- Highlight `HDR Vaginal Cylinder Consult` from the list. Then, hit `Ok`
- Again, place physician under 'Supervisor' and **uncheck `Completed`**
- Add in the following information to the blanks of the template:
	- **Treatment Length**: 4cm (Always for Dr. Farach)
	- **Diameter of Cylinder**: X cm (As Measured When Planning)
	- **Dose to Depth of Vaginal Tissue**: 600cGy to a depth of 0.0cm (Per-Fraction Dose For Solely HDR Brachy I.E. 600cGy Rx For Each Fraction; Depth is 0.0cm because prescription is to SURFACE of cylinder)
	- **D2cc Bladder Dose**: cGy (Found on 'Plan - COMBO' PDF, on page with orthogonal views)
		- **Note:** Divide the value by 5 and input per-fraction dose here
	- **D2cc Rectum Dose**: cGy (Found on 'Plan - COMBO' PDF, on page with orthogonal views)
		- **Note:** Divide the value by 5 and input per-fraction dose here
- Once finished, hit 'Ok' _(NOT 'Sign Off')_

![[Pasted image 20250825174647.png|center|500]]

> [!note] The dose values in this document will need to be **adjusted** if Dr. Farach modifies the isodose lines later during plan review (i.e., recalculate dose, re-acquire all four deliverable documents and combined PDF, upload the new "Plan - COMBO" to the patient under "Documents," and finally update the doses in this document)

>[!note] In some cases, the document choices may not show HDR Vaginal Cylinder Consult. One possible reason is the institution or hospital to which the patient was assign. The available files are institution-dependent. If this is the case, ensure that you select HMH.
### 25. 'Tx Plan HDR Note - HMH' document (HDR Brachytherapy Treatment Plan Note)

**Purpose:** To explicitly report use Of Mobius secondary calculation

- Hit `New` in the top left corner. Then, click `Template` in the bottom left of the embedded Word document that appears. `Check Show All Templates`.
- Highlight `Tx Plan HDR Note - HMH` from the list. Then, hit `Ok`. 
- Place Physician Under `Supervisor` AND **Uncheck `Completed`**.
- Fill Treatment Plan Information:
	- **(2D, 3D Plan)**: 3D Plan *(Because a CT-Sim Is Used As The Basis of Treatment Planning)*
	- **No. of Channels**: 1 _(Because Only 1 Channel In Cylinder)_
	- **No. of Basic Dosimetry Calculations**: 1 *(Because Secondary Dose Calculation Via Mobius Was With ONE Reference Point Only)*
- Once finished, hit `Ok` (NOT `Sign Off`)
## Scheduling The Plan
### 26. Schedule the treatment and Imaging Course

- Go to `Quicklinks` > `Treatment Management` > `Plan Scheduling`.
- On the display that appears, hit **Shift+Click Drag** across as many boxes as there are fractions in your plan (ex: In `Scheduling Overview` Panel). 
- Then, click `Insert` to add the blue boxes representing **the amount of fractions in the entire treatment process**. Finally, hit the `Save` icon ![[Pasted image 20250821132809.png]]above this panel.

![[Pasted image 20250821131734.png|center|300]]

### 27. Billing - Charging For Physics Tasks Occurring

- Access EMR Summary
- Go to **Quicklinks > EMR > Summary**
- Click on `Tasks` tab (next to `Appointments`) ![[Pasted image 20250827102332.png]]
- Click the `New` button ![[Pasted image 20250827102257.png]] 
- Got to the `Activity` box highlighted orange and choose `Prepare Plan` from the drop-down menu
- Add physics Information
	- Click `Add` underneath the orange box below `Activity`
	- Find and highlight `Physics` in `Resource/Staff` menu _(top left section)_ and add it over to right side ![[Pasted image 20250827103320.png]]
	- In the `Staff` list below, find **your name** and add it over to the right. There, checkbox your name. Hit `Ok` at the bottom to close the panel.
	
![[Pasted image 20250827103001.png|center|400]]
- Complete Status
	- Near the bottom _(Before the `Questionnaire` section)_, set the `Status` to `Completed`. ![[Pasted image 20250827103916.png]]
	- Finally, click `Ok` at the bottom of the `Task Dialog`
- Capture Activity
	- Back in the `Tasks` tab for the patient, scroll down the top list of activities to the `Prepare Plan` you just created/added to it. 
	- Right click it and choose 'Activity Capture!'.

> [!warning] Do not follow the billing steps if only practicing how to make a cylinder plan

- Before moving forward, open up the **charge manual** logging billing codes via **(Physics Drive) > 1. Methodist Dunn > HDR Main > Charge Manual**. 

![[Pasted image 20250827133208.png|center|200]]

- Then, go to **'HDR Vaginal Cylinder'** page within the excel sheet _(There is a sheet for every technique)_. 
- Write down / take mental note of **ALL** codes in `CPT` column within the `Plan Day` section that have `PHY` as the responsible party in the far right column.
- Add Procedure Codes
	- Back on the window that was opened in Aria, click 'Add More Procedure Codes' on the middle-right. 
	- Check the 'Show All Procedure Codes' box.
- Enter Billing Codes
	- Find **ALL** the codes recorded in Step 64 from the Excel sheet. Check their boxes in and hit 'Ok'. They should appear in green under 'Procedure Code Details'.
- **NOTE: If A CT-Sim Is utilized for planning, check box 77295 INSTEAD of any of the three 7731X Boxes**
- Lastly, click `Save Edits` at the bottom of the window once codes are added.

---

---
## Final Task(s)

### 28. Create plans for the next fractions and adjust the date

- Copy Previous Plan
- Go to **Quicklinks > Treatment Planning > Brachytherapy Planning** and open up the course you planned for the patient again.
- Right click your **PLAN** _('HDR Cyl___cm')_ and click 'Copy Plan'. 
- Right click your **COURSE** _(`C1a`)_ and click 'Paste Plan'. 
- Re-name new plan ID to **'Cylfx___'** _(Fill In Whichever Fraction You're On)_.
- **Note:** Adjust the date of the plans to ensure that the source is decayed correctly for each fraction
	- This can be done by updating the date in the properties of the plan

![[Pasted image 20250827145306.png|center|600]]

### 29. Generate Brief Report

- Click **Window > Brief Report Window**. This will display the **brief report** for the new plan. 
- Click **CTRL+P** for print options and select **'Microsoft Print to PDF'** from the list in the 'Name' field and hit 'Ok'. 
- Re-name this saved plan as `DecayCalc_CYL_XXmm_FxN` (here XX is the size of the cylinder in mm and N is the fraction number, ex: DecayCalc_CYL_25mm_Fx2) in your patient folder _(see the Post-Planning Documentation section)_.

![[Pasted image 20250827154516.png|center]]
### 30. Upload fraction report on the day of each fractional treatment

- **On the day of the next treatment**, go to **Quicklinks > EMR > Documents** for the patient. 
- Click `Import` and go to the patient folder. 
- Highlight `DecayCalc_CYL_XXmm_FxN` and click `Open`.
- Once the document is pulled up, edit the following details at the top under 'Patient Document Details':
	- **Authored By**: (Look Yourself Up)
	- **Supervised By**: Dr. Farach
	- **Document Type**: Treatment Plan - Decay Calc
	- **Template Name**: "Cylinder Fx___"
- **UNCHECK `COMPLETED` on top right 
- Once finished, hit 'Ok' _(NOT 'Sign Off')_.

--- 
## Planning without templates - For Resident Training ONLY

### 1. Follow Step 9 in the instructions above
### 2. Insert new plan

- Highlight the course and click **Insert** > **New Plan**. 
- Click 'Next' with most recent course highlighted 
- Highlight the treatment prescription you just created. Check 'Select' to the right to attach the created prescription and hit `Next`.
- Highlight the cylinder as the target and hit `Next`
- Enter the following information on `Plan Properties` window
	1. **ID & Name**: "HDR Cyl___cm"
	2. **Protocol Plan**: Cylinder Dunn\Cylinder
	3. **Target Volume**: Cylinder
	4. **Technique**: Intracavitary
	5. **Treatment Percentage**: 100%
	6. **Dose per Fraction**: 600cGy
	7. **Number of Fractions**: 5
- Hit 'Ok' after this.
### 3. Orient cylinder and set User Origin

- As in step 11 above, rotate sagittal and coronal planes to ensure that the cylinder is roughly vertical.
- Define the user origin as the tip of the applicator as in the steps above
### 4. Insert the applicator

- Going to the default view, click **Insert** > **New Applicator** > **Bravos - Dunn**. 
- Then, change ONLY the following into the 'Applicator Properties' window:
	- **Channel Length**: 125 _(ALWAYS for HMH CYLINDERS)_
	- **Step Size**: 0.5cm
	- **1st Source Position**: 0.3cm
	- **Last Source Position**: 4.3cm 

![[Pasted image 20250828133228.png|center|300]]

- Hit 'Ok' after this. The applicator placement icon should now be next to your mouse.
### 5. Draw the applicator

- Two-point method
	- After you insert the applicator, the button for drawing the applicator ![[Pasted image 20250828135254.png]] becomes active.
	- Navigate to the tip of the applicator in the axial plane (right at the slice where the low intensity cavity vanishes) and click in the middle of the channel. This will define the end of your source positions.
	- Move inferiorly to the beginning of your applicator again using the axial plane view. Once you reached the base of the applicator, click on the middle of the central cavity to define the starting point of the applicator. 
		- Note: This method will avoid the need to adjust the angle of the resulting applicator indicator line

![[Pasted image 20250828140014.png|center|400]]
- Arjit's method
	- Ensure a proper rotation for the applicator (the channel should be vertical)
	- Use the Contour Editor button ![[Pasted image 20250828135254.png]] to draw the applicator by clicking on multiple points along the central channel until you reach the end.

### 6. Add a reference line

- Highlight the CT study (ex: `CT_1`) in the left panel. 
- Go to **Insert** > **New Reference Line** and hit `Ok`
- On the coronal plan containing the User Origin, click along the surface of the applicator starting on one side and ending on the other.
	- Note: You want to start and end at the level of the last dwell position.
- Once finished, click `Selection Tool` ![[Pasted image 20250828140836.png]] in the top toolbar again to get out of reference line mode.

![[Pasted image 20250829145210.png|center|200]]
### 7. Calculate the initial dose

- Go to **Planning** > **Modify Dose** > **VEGO TG-43Volume Optimization** in the toolbar. 
- Click 'Ok' at the pop-up stating normal tissue structure has been created. 
- Apply the following:
	- **Slide 'Smoothness' meter to MIDDLE of meter** _(Top High = Coarse, Top Low = Finer DVH)_
	- **Set Up Objectives As**:
	    - i) Highlight 'Reference Line'. Then, click 'Add Upper & Lower Objective'. ![[Pasted image 20250828150115.png]]
		    - Enter 3000 cGy as the desired dose to reference line _(ex: prescription amount per fraction)_ and hit 'Ok'.
	    - ii) In the lower objective
		    - Change the volume to 99%
		    - Keep dose at 3000cGy/100%
		    - Keep priority at 100
	    - iii) In the upper objective
		    - Change the volume to 1%
		    - Change dose to 3005cGy/100.17%
		    - Keep priority at 100
- Click "Optimize" to run. 
- Click on the Calculate 3D dose  ![[Pasted image 20250828153708.png]] button 
### 8. Modify the isodose level display 

- Follow the instructions in step 12
### 9. Shape the dose as needed

- Click on 'Dose Shaper' on the top toolbar ![[Pasted image 20250828154526.png]]. 
- Right click anywhere in the orthogonal views and slide over to 'Local' in the 'Dose Shaping Effect' window that appears. 
- Then click 'Ok'. 
- Go to your frontal/sagittal views and **Click CTRL + Drag** near the 100% red isodose line to shape it onto the cylinder surface. 
- Additionally, you may also find 'Dose Re-Scaler' useful if the isodose line is symmetric but not aligned with the cylinder surface _(allows proportional scaling of dwell times to retain shape)_. Once satisfied with the dose distribution, save the plan.

---
## Case Study: Improper positioning of the template

In this example, the template was position inferior to the correct location. The end of the digitized channel should coincide with the end of the channel's cavity (low attenuation or dark region in the middle of the cylinder). 


![[Pasted image 20250822165650.jpg]]
