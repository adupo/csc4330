This is the testing document

Test Case ID: 1
----------------
Test Case Name: Access Website <br />
Designed By: Blake Allen <br />
Executed By: Blake Allen <br />
Priority: High <br />
Short Description: Test the ability to access website <br />

Pre-Conditions: The user must have a stable internet connection through an internet browser <br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Type the website address into a browser | DuoMonkeyEditor.com|The system displays the home page for DuoMonkeyEditor | |
 <br />
Post-Conditions: Any changes the user makes on the website are now stored in the database
 <br />
Test Case ID: 2
---------------
Test Case Name: Login  <br />
Designed By: Aaron Dupont  <br />
Executed By: Aaron Dupont  <br />
Priority: High <br />
Short Description: Test the login feature with correct login information <br />

Pre-Conditions: User must have a valid Google username and password <br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click the 'Get Started Here' buton | | The system presents a popup with username and password input fields|If the user is already logged in, they will not be able to login again|
|2|Enter username |'googleusernamehere' |The input field will display the entered username | |
|3|Click the 'Next' button| |The system presents an input field for the password | |
|3|Enter Password |'googlepasswordhere' |The input field will hide the entered password| |
|4|Click 'Sign In' button| |The system presents the user with the chat feature | |
 <br />
Post-Conditions: The user is now logged in to the system. The user can now use the text editor and chat features. <br />
 
 Test Case ID: 2.1
------------------
Test Case Name: Login (Incorrect Username) <br />
Designed By: Aaron Dupont <br />
Executed By: Aaron Dupont <br />
Priority: High <br />
Short Description: Test the login feature with incorrect username <br />

Pre-Conditions:User must have an incorrect username <br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click the 'Get Started Here' buton | | The system presents a popup with username and password input fields|If the user is already logged in, they will not be able to login again|
|2|Enter incorrect username |'incorrectgoogleusernamehere' |The input field will display the entered username | |
|3|Click the 'Next' button| |The system presents an error message that reads 'Sorry, Google does not recognize that email' | |
 <br />
Post-Conditions: The user is not logged in to DuoMonkeyEditor. The user is still presented with the enter username dialog popup <br />
 
 Test Case ID: 2.2
------------------
Test Case Name: Login (Incorrect Password) <br />
Designed By: Jason Lee <br />
Executed By: Jason Lee <br />
Priority: High <br />
Short Description: Test the login feature with incorrect password <br />

Pre-Conditions: User must have an incorrect password <br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click the 'Get Started Here' buton | | The system presents a popup with username and password input fields|If the user is already logged in, they will not be able to login again|
|2|Enter username |'googleusernamehere' |The input field will display the entered username | |
|3|Click the 'Next' button| |The system presents an input field for the password | |
|3|Enter incorrect password |'incorrectgooglepasswordhere' |The sytem presents an error message that reads 'Wrong password. Try again.'|After entering a distinct incorrect password 10 times, the user is presented with a captcha|
 <br />
Post-Conditions: The user is not logged in to DuoMonkeyEditor. The user is still presented with the enter password dialog popup.
  <br />
 Test Case ID: 3.1
-------------------
Test Case Name: Chat Invite To Session <br />
Designed By: Blake Allen <br />
Executed By: Blake Allen <br />
Priority: Medium <br />
Short Description: Test the ability to invite a visitor to your session <br />

Pre-Conditions: The user must be logged in to DuoMonkeyEditor <br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click 'Visitors' dropdown box | |The system displays a list of current visitors in the dropdown | |
|2|Click another visitors name from the 'Visitors' dropdown list| |The system displays a popup labeled 'Private Invite' that shows 'Invite' and 'Cancel' buttons| |
|3|Click 'Invite' button ||The system displays a popup labeled 'Invite' with 'Accept' and 'Decline' buttons  on the invited users screen| |
|4|Other visitor (invited visitor) clicks 'accept' button on the popup labeled 'Invite'| |The system now displays a new tab in the chat window that reads 'Private Chat' | |
 <br />
Post-Conditions: The user is now in a chat session with the invited user <br />

 Test Case ID: 3.2
------------------
Test Case Name: Chat (Invite To Session: Inviting User Cancels) <br />
Designed By: Blake Allen <br />
Executed By: Blake Allen <br />
Priority: Low <br />
Short Description: Test the ability to cancel a private invite <br />

Pre-Conditions: The user must be logged in to DuoMonkeyEditor <br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click 'Visitors' dropdown box | |The system displays a list of current visitors in the 'Visitors' dropdown | |
|2|Click another visitors name from the 'Visitors' dropdown list| |The system displays a popup labeled 'Private Invite' that shows 'Invite' and 'Cancel' buttons| |
|3|Click 'Cancel' button ||The system removes the popup labeled 'Private Invite'| |
 <br />
Post-Conditions: The user is viewing the 'Visitors' dropdown with a list of current visitors <br />

 Test Case ID: 3.3
------------------
Test Case Name: Chat (Invite To Session: Invited User Cancels) <br />
Designed By: Kevin Elizabeth <br />
Executed By: Kevin Elizabeth <br />
Priority: Low <br />
Short Description: Test the ability to decline a private invite <br />

Pre-Conditions: The user must be logged in to DuoMonkeyEditor <br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click 'Visitors' dropdown box | |The system displays a list of current visitors in the dropdown | |
|2|Click another visitors name from the 'Visitors' dropdown list| |The system displays a popup labeled 'Private Invite' that shows 'Invite' and 'Cancel' buttons| |
|3|Click 'Invite' button ||The system displays a popup labeled 'Invite' with 'Accept' and 'Decline' buttons  on the invited users screen| |
|4|Other visitor (invited visitor) clicks 'decline' button on the popup labeled 'Invite'| |The system now displays a popup on the inviting user's screen that reads 'username has declined your invite' | |
 <br />
Post-Conditions: The user is viewing the 'Visitors' dropdown with a list of current visitors <br />

 Test Case ID: 4
----------------
Test Case Name: Chat Messaging <br />
Designed By: Wilson Zhu <br />
Executed By: Wilson Zhu <br />
Priority: High <br />
Short Description: Test the ability to send messages in the chat feature <br />

Pre-Conditions: The user must either be in a 'Private Chat' or in a 'Chat Room' <br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click the text box labeled 'Your Message' | |The system now shows a blinking cursor in the text box with a background message of 'Type your message here...' | |
|2|Type message|'A sample message would be written here.' |The system will display characters as they are typed | |
|3|Press the 'Enter' key | |The system displays the name, time-stamp, and message contents in the chat window | |
 <br />
Post-Conditions: The message is now displaying on each parties screen. The message has been saved in the database and can be viewed after logging in. <br />
 
  Test Case ID: 5
-------------------
Test Case Name: Logout <br />
Designed By: Aaron Dupont <br />
Executed By: Aaron Dupont <br />
Priority: Low <br />
Short Description: Test the ability to logout of the DuoMonkeyEditor web application <br />

Pre-Conditions: The user must be logged into DuoMonkeyEditor application <br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click the button labeled 'Logout'| |The system redirects the browser to the DuoMonkeyEditor homepage | |
 <br />
Post-Conditions: The user is being presented with the DuoMonkeyEditorHomepage <br />
