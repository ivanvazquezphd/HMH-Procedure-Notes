## Phase 1. Prescription

1. Go to `Quicklinks` > `Treatment Management` > `Prescribe Treatment`

2. Create a **new Course** by clicking on the drop down arrow ![[Pasted image 20250918105526.png]] and selecting `New`

![[Pasted image 20250918105510.png|center|250]]

3. Enter the course name, ex: C1a if first or C2a if second HDR treatment, and the intent

![[Pasted image 20250918105758.png|center|400]]

4. Select the `HDR Prostate Boost(Shared)` if boost or `HDR Prostate\SV (Shared)` if monotherapy for your template ![[Pasted image 20251023105558.png|250]] 
	- This will populate the fields in the Treatment Prescription pane (ex: assign One Fraction)

![[Pasted image 20251023114000.png|center500]]

## Phase 2. Contouring

> [!tip] Prior to contouring, we should have an image with the... 

![[Pasted image 20251023125752.png]]

8. For the first fraction, the physician typically uses a fused image-pair to delineate the prostate. Currently, we fuse the CT with another modality (ex: MRI or PET) to help. 
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