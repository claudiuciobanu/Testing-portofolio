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

**Actual Results:** Please notice that the changes the User made are not saved.

**Expected Results:** The changes the User made in Options Menu must be saved even after a title restart.

**Notes:**
 - The issue does not occur on "Y" game and "Z" game, the title will correctly save the changes made in options menu even after a title restart.

---

### B) **Summary:** Controller disconnect message is overlapped by button prompts

**Steps to reproduce:**
1. Boot the title
2. Proceed to "Y" game
3. Disconnect controller

**Actual Results:**
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

**Actual Results:** 
Please notice that the changes the User made are not correctly kept when transitioning to Gameplay, the title will change  modify the Combat Difficulty to default (initial) settings.

**Expected Results:**
The settings set up made in the "X" or "Z" Main Menu -> Extra screen must be kept when transitioning to active gameplay.

**Notes:**
 - The issue does not occur on "Y" game.

---

# Test Cases Samples

### A) **Test Case title:** Set JavaScript on Google Chrome

**Summary:** Configure correctly JavaScript settings on the  Google Chrome browser.

**Steps to reproduction:**
 1. Install Google Chrome.
 2. On your computer. open Google Chrome.
 3. At the top right, click "Customize and control Google Chrome" (the three points vertically).
 4. Click Privacy and Security.
 5. Click Site settings and go bottom to the Content.
 6. Click to JavaScript and click the button from the right (on the same line with "Blocked").

**Expected results:**
The user should can see the blue button and JavaScript must be changed from "Blocked" to "Allowed".

---

### B) **Test Case title:** Testing JavaScript on browser

**Summary:** Checking if JavaScript runs after the settings from browser are set correctly.

**Steps to reproduction:**
 1. Go to "www.sublimetext.com".
 2. Go to Download.
 3. Choose the right version for your OS and download it.
 4. Install the version you downloaded.
 5. Open SublimeText.
 6. Copy-Paste to this code:<FORM><INPUT TYPE="text" VALUE= "Settings are ok!" NAME = "button"onChange= "alert('Please do not change the settings')"></FORM>
 7. Press CTRL + S.
 8. At the File Name put the name "index.html" and click Save.
 9. Go to the saved file (index.html) and right click on it. 
10. Open with Google Chrome.

**Expected results:**
The user should receive an informative field that the settings are ok and JavaScript runs.

---

# Postman tests

### A) Testing status and response data

     //testing status
pm.test("Status test", ()=>{

 &nbsp;&nbsp;&nbsp;  pm.response.to.have.status(200);

});

    //testing if the response for "q" key is equal to Targoviste
const jsonResponse = pm.response.json();

pm.test("Testing response for town", () => {

  &nbsp;&nbsp;&nbsp; pm.expect(jsonResponse.name).to.eql("Târgoviște");

});

    //testing if the weather[0].main is equal to "Rain"
pm.test("Testing response size for main", ()=>{

  &nbsp;&nbsp;&nbsp; pm.expect(jsonResponse.weather[0].main).to.equal("Rain");

});

### B) Testing response time and data type

    //testing the response time
pm.test("Response time is less than 200ms", () => {

  &nbsp;&nbsp;&nbsp; pm.expect(pm.response.responseTime).to.be.below(200);

});

    //testing if sys.id result from the response is a number
pm.test("Test data type", () => {

  &nbsp;&nbsp;&nbsp; pm.expect(pm.response.json().sys.id).to.be.a("number");

});

    //testing if weather[0].description has the value "clear sky" and if weather.find is an object
const jsonData = pm.response.json();

pm.test("Test array properties", () =>{

   &nbsp;&nbsp;&nbsp; pm.expect(jsonData.weather[0].description).to.include("clear sky");

   &nbsp;&nbsp;&nbsp;const cloudsWeather = jsonData.weather.find

  &nbsp;&nbsp;&nbsp; (m => m.main === "Clear");

  &nbsp;&nbsp;&nbsp; pm.expect(cloudsWeather).to.be.an("object");

});
