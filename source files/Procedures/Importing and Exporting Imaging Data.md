
This report convert a .... including creating a new patient 
# Importing Imaging Data 

1. Go to Quicklinks > DICOM > Import Export >`DICOM Media File Import Filter` and click the 'Next' arrow ![[Pasted image 20250915165942.png]]

![[Pasted image 20250915165923.png|center|500]]

2. The window should now display patients recently exported to Eclipse (e.g., patients CT-simulated during the day). Click the relevant patient for your case and the corresponding image sets will display.

![[Pasted image 20250925120222.png|center|600]]

3. Ensure the desired data is selected and click `Import Selection`

4. If this is a new patient, click on `New Patient...`
## Creating a New Patient

![[Pasted image 20250925122057.png]]

5. 'Next' again. If a list of notices appear on the window, bubble in 'Error' to see if there are any. If not, just 'Yes' to continue the image conversion. Finally, hit 'Next' again to connect the CT to the patient. You will then reach the summary page.

create connections

6. Go to Quicklinks > Treatment Planning > Contouring for the patient. The CT series of correct date should be here now. Right click it to go to 'Properties'. Then, rename the 'ID' to 'C1a' - **put the appropriate fraction number in the blank. This will ensure the correct CT series is used for the next fraction's plan without mix-up.**

> [!warning] When importing new CT scans, verify both the scan date and sequence number. The system typically assigns "3" to the first CT scan (scans 1-2 are usually AP and Lateral topograms). If applicator adjustments are made based on initial scan results, additional scans may be acquired, resulting in multiple CTs (e.g., CT 3 and CT 4) being sent to Eclipse. Always use the highest-numbered/most recent scan for treatment planning, as it reflects the final applicator positioning.
> 
> **Essential Rule:** Latest scan = final applicator position = correct planning dataset


