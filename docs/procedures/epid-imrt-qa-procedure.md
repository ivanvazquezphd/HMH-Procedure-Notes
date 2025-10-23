# EPID IMRT QA Procedure Notes

> **NOTE:** Check all fields of each QA plan to ensure they are not oversized for the EPID, otherwise the electronics will be irradiated! In this case, MapCheck/ArcCheck QA must be done (Dimensions must be <25x20 e.g. X<25 & Y<20; less if collimator is rotated)

## Creating a Verification Plan for IMRT QA

_Ensure the plan is unapproved first (Right Click Plan > Plan Approval). Highlight the intended plan for QA and go to 'Planning > Create Verification Plan'. Then..._

1. Highlight the EBT course your plan is under & click 'Next'.
    
2. Select 'Portal Dose Prediction' under 'Verification Method'.
    
3. Set SID=100cm _(for Varian Edge)_. Click 'Next'.
    
4. Ignore Gantry/Collimator/Couch Settings under 'Field Geometry' _(i.e. leave unchecked)_. Checkbox 'Use Tolerance Table' and select 'Physics' from the drop-down menu.
    
    _**This tolerance limits table translation with each fraction & alerts if outside tolerances**_
    
5. Set number of fractions to 1 _(only running QA once)_ and click 'Next'.
    
6. Click 'Finish' and the verification plan will be created.
    
![[Pasted image 20250829074058.png|center|400]]
## To Prepare & Export the Plan to the Linac...

7. **Plan-approve** your verification plan in the EBT Planning workspace you are still in.
    
8. Go to 'Treatment Preparation' workspace for your patient. Ensure the 'QA' course is selected at the top _(to the right of the save icon)_. Here, verify the couch and EPID imager parameters are set as shown in the image. Change them if necessary & hit save. _(Step 8 Image)_
    
9. Go to 'Plan Scheduling' workspace for your patient and expand the verification plan. Highlight the box next to your plan and click 'Insert'. It should fill in as blue. Then, highlight all the boxes next to the plan's arcs simultaneously. Right click on the highlights and select 'Add Imaging'. Select 'Portal Dosimetry'. Close the patient. _(Step 9 Image)_
    
10. Now, go to the Aria Schedule for the machine QA is to be run on. Schedule the patient on any open time slot of the machine at/before the time of QA. Designate the activity as 'Calibration'.
    
    _**This will allow the patient/plan to show up at the machine for QA**_
    
    _(Step 10 Image)_

## Conducting IMRT QA at the Machine

11. Go over to the machine and place the couch at _~15cm vertical, ~16cm longitudinal, & ~0cm lateral position_ (to prevent collision with the gantry during QA).
    
12. Go over to the console and enter **TREATMENT MODE**. This is where IMRT QA is run from.
    
13. Click the 'Open' folder and locate the patient you scheduled for QA _(you may have to refresh it)_. Scroll to their QA plan and checkbox it. Then click 'QA' in the bottom right to load the plan.
    
14. Click on the first arc _(i.e. skip any imaging)_ & hit 'Prepare' on the console. The machine will then prompt you to motion-enable it and allow the gantry, collimator, and couch to move into position. _Click 'Machine Override' and checkbox the couch positions that the machine wants to go to._ Then click 'Apply' and enter your login to confirm. _(Step 14 Image)_
    
15. Add automation if desired and deliver all arcs of the QA plan. Then close out of the patient on the machine console.
    
16. On a **separate** computer at the treatment console, open up the patient in Eclipse and go to the 'Portal Dosimetry' workspace. Here, conduct the following steps for the fluence maps collected for each arc:
    
    i. Highlight any arc's fluence map and **Right Click > Create Composite Image**.
    
    ii. Checkbox **ALL** fluence maps for the QA plan and click 'OK'.
    
    iii. With the composite image now displaying, move the digital graticules (red) to the **hottest region** of the fluence map that you can find. Then, go to the bottom line plot and _make note of the maximum CU value for the yellow/green lines._
    
    iv. Go to the bottom panel and click 'Options'. Here, set the Gamma Analysis to (3%, 2mm) for regular VMAT. _**NOTE:** The Gamma Analysis is conducted at (2%, 2mm) for SBRT._
    
    ```
    Additionally, checkbox 'Average Dose Diff.' and enter **5% of the maximum CU value that you observed.** Then, click 'Ok'.
    ```
    
    v. Click 'Perform Analysis' now that all the settings are applied. _Make note of the 'Avg. Dose Difference' value that displays in green._ Click the 'Save' icon in the upper left _(Under 'File' on the toolbar)_. _**NOTE:** The gamma analysis should be >90% pass rate. If not, do NOT continue and inform another physicist._ _(Step 16 Image)_