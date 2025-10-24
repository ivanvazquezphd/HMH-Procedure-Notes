---
layout: default
title: HDR Daily QA
---

# HDR Daily QA Procedure

Created by **Ivan Vazquez** in collaboration with **Arjit Baghwala**

> **⚠️ Key Objective of Daily QA**
> 
> Ensures accurate source positioning, dwell time, and proper functioning of the afterloader to guarantee safe, precise delivery of treatment as well as patient and personnel safety. After completion, the physicists would have verified that all safety features in treatment and control rooms function properly.

## Control Room Setup

### 1. Initial Power-Up and System Checks
- Ensure that the **wall switch** is set to HDR (1)
- Turn on all **cameras** and scan the room (2)
	- This checks if `Video Monitor/Intercom` are functional
- Turn on the **personal dose monitor** by holding down the power button (3)
- Turn on the radiation **survey meter** (4)

<p align="center">
  <img src="{{ site.baseurl }}/attachments/Pasted image 20250918210821.png" alt="Control Room Setup" width="650">
</p>

- Find the **console key** and **switch the system to on**
- Note the date, time, and **source activity/strength** shown by the program
	- This check if the `Date/Time on Console Correct`
- Check **battery level** on displayed on the GUI (UPS Status)
	- Check if UPS battery is more than 90%

<p align="center">
  <img src="{{ site.baseurl }}/attachments/Pasted image 20250901134029.png" alt="Console Display" width="400">
</p>

> **📝 Note:** You will log the activity in TotalQA, so note the value or take a picture before leaving the control room if you are filling out your report in a different room

### 2. Prepare a Test Plan
-  **Log in** using your credentials
- **Prepare the Test Plans** before you walk into the room
	- Click on `Test Plans` > `4DailyQA` and proceed 
		- **Note:** The number in front of DailyQA will change after the maximum number of fractions for the test plan are delivered (n=99)

<p align="center">
  <img src="{{ site.baseurl }}/attachments/Pasted image 20250925080722.png" alt="Test Plan Selection">
</p>

> **📝 Note:** We run a test plan that can only be used 99 times. Once exhausted, we need to create a copy of the plan. The way it is done in our clinic, is to create a copy with the next ascending number.

### 3. Treatment Room Setup

- Enter the treatment room with the survey meter each time
- Ensure that the emergency container ("lead pig") is located in the room (1)
- Grab the lock key and Perma-Doc from the cabinet 
- **Unlock the two exterior locks** on the cabinet (enter authorized PIN)

<p align="center">
  <img src="{{ site.baseurl }}/attachments/Pasted image 20250918210528.png" alt="Cabinet Locks" width="600">
</p>

- Use the key (2 in the figure on the right) to unlock the afterloader's lock, which allows you to remove the chain 
- Roll out the CamScale and position it in line with the treatment bed facing the gantry (see picture below)
- Roll out the afterloader and position it in from of the CamScale parallel to the couch on the side closer to the gantry (see picture below)
- Connect the ethernet cable of the CamScale to the wall port inside the storage 
- Align the CamScale ensuring that the laser line remains within the region of tolerance marked on the afterloader (see the picture)

> **ℹ️ Info:** You should make an effort to remain consistent with your setup. The results from the CamScale can fluctuate based on the position of the afterloader

- Connect the trasfer tube in the CamScale storage compartment (black tube) to channel 1

> **⚠️ Warning:** Ensure you do not flip the CamScale's transfer guide by ensuring that the end of the tube at the top of the storage is connected to the afterloader while the bottom end connects to the CamScale.

- Connect one of the transfer guides on the wall to the Perma-Doc

<p align="center">
  <img src="{{ site.baseurl }}/attachments/Pasted image 20250909205750.png" alt="CamScale Setup" width="500">
</p>

<p align="center">
  <img src="{{ site.baseurl }}/attachments/Pasted image 20250909210029.png" alt="Transfer Guide Connection" width="500">
</p>

## Safety Checks

### 4. Length Verification

- With the plan loaded on the afterloader, run the length verification (132cm ± 1mm)
	- If the test plan was not prepared prior to entering the room, you will need to return to the control room and prepare it it 
- Prior to leaving the room, partially disconnect the transfer guide connected to the perma-doc 
- Start the `Last man out` sequence on the way out of the room 
- Confirm that a patient is not in the treatment room

### 5. Check Obstruction Detection Functionality

- Run the QA plan from the control room
	- If the obstruction detection functionality is working correctly, the system will detect an obstruction in channel 2
- Return to the room and properly connect the transfer guide 
- On the way out, restart the last-man-out sequence

### 6. Time the First Dwell Time and Check the PrimAlert Monitor

- Run the QA plan with the transfer guide properly connected
- Start the two timers once the source wire (yellow indicator) reaches the first dwell position 
	- The source is at this position for 30 seconds, which gives you time to check that the PrimAlert monitor is blinking
- Stop the time once the source leaves the first dwell position
	- Both timers should read 30 seconds

<p align="center">
  <img src="{{ site.baseurl }}/attachments/Pasted image 20250902081957.png" alt="Timer Display" width="400">
</p>

### 7. Test the Interrupt Button 

- **Click the `Interrupt` button on the graphical interface** after the source leaves the first dwell position
	- This should interrupt the treatment and park the source
	- You should see the PrimAlert monitor lights turn off

### 8. Check the Key Interlock

- Restart the delivery of the QA plan and wait for the source to reach a dwell position
- **Turn the key to the middle position** to interrupt the treatment

> **⚠️ Warning:** Turning the key to the off position will terminate the test, which will require a repeat of all interruption tests

### 9. Door Interlock Functional

- Restart the delivery of the QA plan and wait for the source to reach a dwell position
- **Open the door** to the vault once the source is out
- Restart the last-man-out sequence

### 10. Emergency Stops Functional

- Restart the delivery of the QA plan and wait for the source to reach a dwell position
- Press the **Interrupt (red) button on the console** to halt treatment

<p align="center">
  <img src="{{ site.baseurl }}/attachments/Pasted image 20250918211604.png" alt="Emergency Stop Button">
</p>

- Clear the error and move to the next screen to sign off on the tests
- Select `Abort this fraction` before clicking `Done`

<p align="center">
  <img src="{{ site.baseurl }}/attachments/Pasted image 20250925082434.png" alt="Abort Fraction" width="350">
</p>

### 11. Source Position Verified

- On the top right (to the left of Log Out), click on the drop down menu/button and select `System Configuration` → `Cable and Source`→ `Proceed`
- Proceed until you reach a window like the one below
- Click on `Prepare Verification` and run the check, your values should be below 0.05 cm

<p align="center">
  <img src="{{ site.baseurl }}/attachments/Pasted image 20250925083708.png" alt="Source Position Verification" width="500">
</p>

### 12. Worklist Check

-  Select `System Configuration` → `Console and Afterloader`→ `System Setting`
- You should see options for `Worklist` and `Treatment` on the bottom left 

<p align="center">
  <img src="{{ site.baseurl }}/attachments/Pasted image 20250925094820.png" alt="Worklist Settings" width="400">
</p>

---

[← Back to Procedures](../procedures.html)
