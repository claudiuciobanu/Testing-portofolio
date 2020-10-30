# Bugs samples

A) Summary: The title does not save the options changes when performing this action during "X" game: Main Menu -> Extras Screen.

Steps to reproduce:
1. Boot the title 
2. Open "X" game  and pass the IIS
3. Notice that GamerProfile save data will be created. (Press PS button -> Highlight the title -> Press "OPTIONS" button -> Select Save Data Management -> Delete -> METR and check that the game profile save data is present. )
4. Enter Extras -> Options -> Select any submenu and make the necessary change
5. Select Confirm Selections and Exit
6. Notice that the title will inform the use that "Saving data do not turn off your system".
7. Exit back to the Launcher or restart the title, after that return back to "X" game and verify the changes made in step 4.

Actual Result: Please notice that the changes the User made are not saved.

Expected Result: The changes the User made in Options Menu must be saved even after a title restart.

Notes:
 - The issue does not occur on "Y" game and "Z" game, the title will correctly save the changes made in options menu even after a title restart.
