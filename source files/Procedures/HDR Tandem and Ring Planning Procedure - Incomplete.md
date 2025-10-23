## Phase 1. Prescription and imaging note

1. Go to `Quicklinks` > `Treatment Management` > `Prescribe Treatment`

2. Create a **new Course** by clicking on the drop down arrow ![[Pasted image 20250918105526.png]] and selecting `New`

![[Pasted image 20250918105510.png|center|250]]

3. Enter the course name, ex: C1a if first or C2a if second HDR treatment, and the intent

![[Pasted image 20250918105758.png|center|400]]

4. Select the `HDR Tande and Ring(Shared)` template  ![[Pasted image 20250918110318.png|250]]
	- This will populate the fields in the Treatment Prescription pane (ex: assign 5 fractions)

5. ==Change the values to those appropriate for the patient being treated as needed. Some values that may change include:==
	- **Prescribe To:** Volume _(Hit 'Add' & Select 'CTV')_ ← **NOTE: MUST match the CTV structure name in the clinical protocol later**
	- **Fractions:** 5 (Monotherapy); 3 (EBT + Brachy) 
		- To check patient's radiation history in our system, go to: `Quicklinks` > `Treatment Management` > `RT Summary` for patient and view all courses in 'Course' or ask the physician
	- **Total Prescribed Dose:** 3000 cGy
    - **Prescribed Dose/Frac:** 600 cGy
    - **Notes:** "Tandem 6 cm 60 degrees" 
	    - You should also note the number of needles used; ex: "Tandem 6 cm 60 degree wing + 2 needles"
	    - ==You can check this by viewing nurse notes in Quicklinks > EMR > Journal OR in Contouring Workspace==
    
![[Pasted image 20250918111000.png|center|600]]

6. The template should have populated the imaging details under `Treatment Management` on the right. You should see `CT: Pre Tx, Every Treatment`
		- If you do not see this in the `Imaging:` field, add Imaging by clicking `Add`> select `CT` > ensure that `Pre Tx` is selected and click `OK`

![[Pasted image 20250918142540.png|center|250]]

![[Pasted image 20250918142241.png|center|400]]

7. Click on `Save as Draft` to save all entries
## Phase 2. Contouring

> [!note] At the time of writing, we create contours manually in the contouring UI in eclipse 

8. For the first fraction, the physician typically uses a fused image-pair to delineate the HR-CTV. Currently, we fuse the CT with another modality (ex: MR or PET) to help. 
	- Navigate to the image registration tab ![[Pasted image 20250925113440.png]]
	- Verify MR availability on the horizontal display of chronological images for the patient
		- If you do not see an MRI, you should check Epic to see the available imaging as well as the notes stating what was used for treatment
		- If the patient note describe the imaging study used to identify the disease, you should try to import that image.
		- It is also good practice to import the most recent study with the same modality, since the anatomy will be most relevant
	- Perform `Auto Matching` ![[Pasted image 20250925152911.png]]  
	    - Click 'Auto Matching' in the toolbar
	    - A list of acquired images will appear for source and target selection
		    - Image Selection:
			    - **Target Image:** Primary planning image (typically the Planning CT with existing contours)
			    - **Source Image:** Secondary planning image (typically Planning MR or Previous Fraction's CT)

9. Add the Tandem & Ring OARs/structures
	- Click on `Structure` > `New Structures From Clinical Protocol` >` T&R & Gyn Dunn` > `Attach...` > `OK`
		- This should add the HR-CTV as well as the sigmoid, rectum, bowel, body, and bladder

10. Change the name of the CT Image to **CT HDR T&R FX 1** 
	- Right click on the `CT Image` box (top left) > selecting Properties > Changing the ID to **CT HDR T&R FX1** (here 1 indicates the fraction number, which may be different in your case)

11. Refer to the [[HDR Cylinder Planning]] notes for instructions on how to get started with contouring. Below is a concise set of tips.
	- To see the structures added with the protocol, hover over the CT display
		- Click on one to enable the contouring tools for that structure
		- Use the Brush and Interpolate Structure buttons (and other tools) as needed
		- Tips: 
			- Contour EVERY 3-4 SLICES for a structure volume. Then, once finished, click `Interpolate Structure` on the vertical toolbar and `Apply` 
			-  Scroll through slices for each structure to check the interpolated slices and make adjustments as needed
	- You can use [[Female RTOG Normal Pelvis Atlas.pdf]] for guidelines 

> [!tip]  Contour about 7cm superior to the tandem's tip AND ~2cm inferiorly from where the BEND in the tandem is


![[Pasted image 20250921131713.png|center|700]]

## Phase 3. Planning

### 3.1 Creating a plan 

> [!note] This must be done before setting the Default Viewing Plane & Origin Location

12. Go to `Quicklinks` > `Treatment Planning` > `Brachytherapy Planning`
13. Open the relevant course and imaging set for the patient
14. Click `Insert` > `New Plan` > Click Your Brachytherapy Course (ex: C1a) > Click `Next >`

![[Pasted image 20250919122206.png|center|400]]

15. Select the relevant RT prescription
	- The prescription build for phase 1 should be visible. Select it and click `Next >`

![[Pasted image 20250919122404.png|center|400]]

16. Select the plan target structure (ex: `HR-CTV`) and click `Next >`

17. The window titled `Plan Properties` should display now. Include the following information

    - **ID**: HDR_T&R_FX **"fx number"**, ex: `HDR_T&R_FX 1`
    - **Protocol Plan**: `T&R & Gyn Dunn\T&R`
	    - When you select the Protocol Plan, a warning message will pop up. Click `Ok`
    - **Target Volume**: `HR-CTV`
    - **Technique**: I`NTRACAVITARY`
    - **Number of Fractions:** `1`

![[Pasted image 20250919143402.png|center|400]]

> [!note] T&R Plans are ALWAYS 1 fraction since we create a new plan with each fraction. Recall that, in HDR Cylinder, the plan's # of fractions is 5 (or 3) and we change it to 1 when sending to Mobius
### 3.2 Views setup and User Origin

18. With the rotation ![[Pasted image 20250921123117.png]] tool selected, reorient the different views to ensure that the portion of the tandem passed the bent (ex: the part in the uterus) is oriented vertically in the coronal and sagittal views as shown in the image

	- It helps to rotate one plane at a time. For instance, you can get the sagittal plane aligned first and then rotate the coronal plan (and axial) as needed
	- Once done,  set the default viewing planes ![[Pasted image 20250921123923.png]]

19. Move the planes to the positions shown in the image (read the description below) and define the `User Origin`
    
    - On **axial** view, crosshairs should coincide with the central tandem axis a short distance superior to the bend in the tandem
	    - This corresponds to a plane slightly above the buildup cap
    - On **coronal** view, vertical crosshair (corresponding to the sagittal plan) should align with the tandem's channel axis while the horizontal crosshair should be appear slightly superior to the **buildup cap**
    - On **sagittal** view, vertical crosshair should be along tandem's channel axis
    
> [!note] If channel within tandem OR buildup cap is not clearly visible, adjust window and level to assist (ex: try the 'Abdomen' preset)
    
20. Once properly oriented, click `Set Default Viewing Planes` in the top toolbar. Then, click `Current` > `OK`

![[Pasted image 20250921093935.png]]

21. Define the **User Origin**
	- Right click ![[Pasted image 20250921141125.png]]
	- Click on `Set User Origin...` 
	- Select `Viewing plane intersection` from the drop down menu and click `Apply` > `OK`
	
![[Pasted image 20250921141239.png|center|400]]

> [!note]  The placement of the user origin is important for defining a reference point (Point 'A') later in planning.
### 3.3. Applicator placement

#### 3.3.1 Tandem

22. Go to `Insert` > `New Applicator` > `Bravos - Dunn` > (Click `OK`)

23. Enter the following information (and hit `OK`):
    - **ID**: Tandem 6cm
	    - Other possible values for the length are 4cm and 8cm
    - **Channel Number**: 1
    - **Channel Length**: 132 cm 
	    - Other relevant lengths to remember include 125 cm for HDR Cylinder and 150 cm for Endobronch catheter
    - **Step Size**: 0.5 cm 
    - **First Source Position**: 0.1 cm (_Dead space at end of channel_)
    - **Last Source Position**: 6.1 cm
	    - First position, 0.1cm, plus 6cm Tandem treatment length

![[Pasted image 20250921141758.png|center|350]]
    
24. Draw the applicator by clicking along the channel 
	 - ==Zoom in on the sagittal or coronal views and click near the top of the applicator to define far end of the digitized applicator==
	- Zoom out and click further down the channel to digitize the rest of the channel
		- Continue digitizing until the track extends some distance beyond the bend (ex: 7- 10 cm)
		- The `Current geometrical length` displays the length of the digitized channel

![[Pasted image 20250921143002.png|center|300]]
#### 3.3.2 Ring

25. Click 'Reset Geometry' in top toolbar to return to default viewing planes

26. Click on `Planning` > `New applicator from library` > `Dunn 60deg Ring`
    
27. Align the template of the Ring applicator with the CT by moving and rotating the applicator ![[Pasted image 20251007133927.png]]
    
    - **NOTE**: If ring is angled and therefore partially visible between slices, you will have to rotate the views until fully in a single axial slice
    - **NOTE**: You may again have to adjust window and level to ensure inner channel is visible

28. Place the **ring applicator** following the steps below
	- On the coronal plane, ensure that an axial slice can visualize the cavity representing the channel. This is the line representing the axial slice intersects the cavities of the ring along a coronal slice as shown in the left figure below
	- Once aligned, zoom in on the **axial view** and click to place the first applicator position (near the end of the ring)
	- Then, click at incremental distances going CCW along the ring's channel. The dwells positions will appear automatically
		- There should be **10 dwells in total** once finished
		
 > [!tip] You may need to scroll inferiorly 1-2 slices at the end of the ring to continue the final dwell placement(s) in the ring region bending down into the next slice (due to the ring's geometry)

![[Pasted image 20250925084843.png|center|700]]

#### ==3.3.4 Additional channels (needles)==

In some cases, the physician may use needles, which need to be digitized following the steps below:
31. Add an applicator
	- Add an applicator for each of the needles (see `Step 22`) 
	- Open the properties (double-click the symbol in the data tree) and update the information:
		- The Channel length should equal the needle + transfer tube (ex: 125 cm)
		- The step size should be 0.5 cm
		- The dead space for Ti needles should be 0.4 cm (4 mm)
		- The first source position should be at 0.1 cm 
		 ![[Pasted image 20250921181243.png|center|450]]
	- Once you add an applicator and update its parameters, you can copy and paste the applicator to get replicas with the same configurations

![[Pasted image 20251007121105.png|center|400]]

>[!warning] When the CT simulation is generated, different techniques such as *using marker wires* or the *removal of the obturator* might be used to help identify the needles. You should used the agreed upon naming/numbering convention when labeling your channels 
 
32. Digitize the needles (applicators)
	- You can digitize manually or with the `Detect applicator from volume image` tool  ![[Pasted image 20250921172714.png]]
	- The first step for both methods should be to **rotate the viewing planes so that the central axis of the needle is (approximately) coplanar** with the sagittal and coronal planes
	![[Pasted image 20251007122128.png|center|400]]
	- **Method 1:** Assisted digitization with `Detect applicator from volume image` tool  ![[Pasted image 20250921172714.png]]
		1. Move the axial plane to a slice there the needle is not entangled with another structure of similar intensity (ex: a slice where the Ti needle is surrounded by low a low intensity region) 
		![[Pasted image 20251007122823.png|center|500]]
		2. Click on `Detect applicator from volume image`  ![[Pasted image 20250921172714.png]] > Click on the region of the image where the needle is located > Click on `Detect Selected`
			- Ensure that the proper settings are selected for the applicator (ex: Metal and Straight for Ti needles)
			- You can adjust the Threshold to influence the accuracy of the detection. If a good value is selected, you should see the region corresponding to the applicator become green on the Threshold window
		3. Inspect the resulting digitization and make changes as needed
			- Tip: You can use the `Draw applicator-plane intersections with given diameter` ![[Pasted image 20251007132003.png]]
	- **Method 2:** Manual digitization with the `Contour editor` tool ![[Pasted image 20251007132130.png]]
		- On the sagittal or coronal plane, click along the length of the applicator to add new sections until a sufficiently long portion (i.e., one including all possible dwell times) is digitized
		- You can click and drag the orange squared to update the digitization
		- Right click an orange square to remove that point from the digitization
		
![[Pasted image 20251007132820.png|center|350]]

### 3.4 Isodose optimization

#### 3.4.1 Point A Method

> [!info] If the physician has yet to draw a CTV onto the CT or you are waiting for a patient MRI to be sent so that the physician can draw the CTV onto the CT-MRI fusion, you can still move forward to calculate dose onto the plan. To do so, follow this sequence: **First** complete Steps 32-37 to place all reference points and record them onto the BED spreadsheet, **then** complete Steps 23-26 to optimize for dose to Point A using the 'Geometrical Optimization' Tool, **next** complete Steps 29-31 to have the physician check plan dose without CTV (ideally it will be drawn during this visit), and **finally** complete Steps 27-28 to fully fill out the BED spreadsheet for this fraction (the physician may stay to evaluate results).

#### 3.4.2 TG-43 Volume Optimization Technique

31. Go to **Planning > Modify Dose > VEGO TG-43 Volume Optimization** in the toolbar. Click 'OK' in the pop-up stating normal tissue structure has been created

32. In the optimization window, apply the following:

	- **Add Objectives**
		- You can use one of three options for this:
			1. Use the `Add from clinical goals` button ![[Pasted image 20251007103833.png]]; number (2) on image below
				- ==This will populate the objectives based on the clinical goals defined in the protocol==
			2. Use the `Import from tamplate` button ![[Pasted image 20251007104012.png]]; number (1) on image below
				- This allows you to search and import clinical goals from a saved template
					- If you add objectives manually, you can save them as a new template using ![[Pasted image 20251007104125.png]]
			3. Set objectives manually using the "objective" buttons ![[Pasted image 20251007104339.png]]
				- For instance:
					- Highlight `HR-CTV 
					- Click 'Add Upper & Lower Objective' ![[Pasted image 20250921164254.png|200]]
					- Enter the prescribed value (ex: 700 cGy) as the desired dose to this structure and hit `OK`
					- In the **lower objective ↗**, change the volume to 99%, keep all other values the same (ex: 100%, 700 cGY, and priority of 100)
					- In the **upper objective ↙**, change the volume to 1%, change dose (ex: 100.14%, 701cGy, priority at 100)
	- **Slide the `Smooth` bar to MIDDLE**
		- This regulates the smoothness of the resulting dose distribution
	- Click `Optimize` to run. Then, click `OK` 
	- Inspect the dwell times, (4) in image below
	
![[Pasted image 20251007103638.png|center|600]]

> [!note] This optimization step will only get us CLOSE to the desired dose distribution. Since the goal with T&R plans is to have a **pear-shaped dose distribution** that meets the prescription and clinical goals (ex: D2cc value limits), you will need to follow the steps below to achieve this
    
33. ==Right click 'Dose' on the left panel and uncheck 'Absolute Dose' (_If selected_), right click 'Dose' again and click 'Isodose Levels'. Here, only two isodose lines check-marked in 2D and 3D. Change their colors to red and white. Finally, designate the white isodose line as 200% relative dose & the red isodose line as 100% relative dose. Then click 'Apply' and 'OK'.

34. Adjust the dwell times as needed to achieve the desired dose distribution and meet dosimetric constraints
	- Go to **Window > Dwell Control Window** from the top toolbar
	- Right click the top right panel and select 'Show Dose Volume Histogram View'. When the DVH appears, go to 'Dose Statistics' in the bottom panel. Enable the HR-CTV and all relevant OARs (bowel, sigmoid, rectum, bladder) so that they will populate the plot
	- Then, go to the 'Clinical Goals' tab at the bottom and remain here for the next step




## TODO: Adding dose without a target using a two point method




## Case Studies

Implanted device...identified by Dr. Kevin Tran


![[Pasted image 20250918152912.png]]