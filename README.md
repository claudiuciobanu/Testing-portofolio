# Bugs samples

### A) **Summary**: The title does not save the options changes when performing this action during "X" game: Main Menu -> Extras Screen.

**Steps to reproduce:**
1. Boot the title 
2. Open "X" game  and pass the IIS
3. Notice that GamerProfile save data will be created. (Press PS button -> Highlight the title -> Press "OPTIONS" button -> Select Save Data Management -> Delete -> METR and check that the game profile save data is present. )
4. Enter Extras -> Options -> Select any submenu and make the necessary change
5. Select Confirm Selections and Exit
6. Notice that the title will inform the use that "Saving data do not turn off your system".
7. Exit back to the Launcher or restart the title, after that return back to "X" game and verify the changes made in step 4.

**Actual Result:** Please notice that the changes the User made are not saved.

**Expected Result:** The changes the User made in Options Menu must be saved even after a title restart.

**Notes:**
 - The issue does not occur on "Y" game and "Z" game, the title will correctly save the changes made in options menu even after a title restart.

---

### B) **Summary:** Controller disconnect message is overlapped by button prompts

**Steps to reproduce:**
1. Boot the title
2. Proceed to "Y" game
3. Disconnect controller

**Actual Result:**
Controller disconnect message "Please reconnect the DUALSHOCK4 wireless controller"  is overlapped by cross and circle buttons. 

**Expected Behavior:**
Controller disconnect message should be dispayed without the buttons overlapping the message.

**Notes:**
- The issue does not occur on "X" and "Z" games.

**Screenshot attached**

---

### C) **Summary:** Certain Gameplay settings made in Front End Menu (Extras) are not kept when transitioning to Gameplay.

**Steps to reproduce:**
1. Boot the title 
2. Open "X" game or "Z" game
3. Enter Extras -> Options -> Select Gameplay and change Combat Difficulty
4. Go back and start a new campaign mission.
5. During Gameplay press the OPTIONS button PAUSE Menu -> Go to Options -> Gameplay and verify if the Combat Difficulty change is kept.

**Actual Result:** 
Please notice that the changes the User made are not correctly kept when transitioning to Gameplay, the title will change  modify the Combat Difficulty to default (initial) settings.

**Expected Result:**
The settings set up made in the "X" or "Z" Main Menu -> Extra screen must be kept when transitioning to active gameplay.

**Notes:**
 - The issue does not occur on "Y" game.

