This is the testing document

Test Case ID: 1
------------
Test Case Name: Access Website
Designed By: Blake Allen
Executed By: Blake Allen
Priority: High
Short Description: Test the ability to access website

Pre-Conditions:
 *The user must have a stable internet connection through an internet browser

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Type the website address into a browser | DuoMonkeyEditor.com|The system displays the home page for DuoMonkeyEditor | |

Post-Conditions:
 *Any changes the user makes on the website are now stored in the database

Test Case ID: 2
------------
Test Case Name: Login
Designed By: Aaron Dupont
Executed By: Aaron Dupont
Priority: High
Short Description: Test the login feature with correct login information

Pre-Conditions:
 *User must have a valid Google username and password

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click the 'Get Started Here' buton | | The system presents a popup with username and password input fields|If the user is already logged in, they will not be able to login again|
|2|Enter Username |'googleusernamehere' |The input field will display the entered username | |
|3|Click the 'Next' button| |The system presents an input field for the password | |
|3|Enter Password |'googlepasswordhere' |The input field will hide the entered password| |
|4|Click 'Sign In' button| |The system presents the user with the chat feature | |

Post-Conditions:
 *The user is now logged in to the system
 *The user can now use the text editor and chat features.
 
 Test Case ID: 2.1
------------
Test Case Name: Login
Designed By: Aaron Dupont
Executed By: Aaron Dupont
Priority: High
Short Description: Test the login feature with incorrect username

Pre-Conditions:
 *User must have an incorrect username

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click the 'Get Started Here' buton | | The system presents a popup with username and password input fields|If the user is already logged in, they will not be able to login again|
|2|Enter Username |'incorrectgoogleusernamehere' |The input field will display the entered username | |
|3|Click the 'Next' button| |The system presents an error message that reads 'Sorry, Google does not recognize that email' | |

Post-Conditions:
 *The user is still not logged in to DuoMonkeyEditor
 *The user is still presented with the enter username dialog popup
 
 Test Case ID: 2.2
------------
Test Case Name: Login
Designed By: Jason Lee
Executed By: Jason Lee
Priority: High
Short Description: Test the login feature with incorrect password

Pre-Conditions:
 *User must have an incorrect 

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click the 'Get Started Here' buton | | The system presents a popup with username and password input fields|If the user is already logged in, they will not be able to login again|
|2|Enter Username |'googleusernamehere' |The input field will display the entered username | |
|3|Click the 'Next' button| |The system presents an input field for the password | |
|3|Enter Password |'googlepasswordhere' |The input field will hide the entered password| |
|4|Click 'Sign In' button| |The system presents the user with the chat feature | |

Post-Conditions:
 *The user is now logged in to the system
 *The user can now use the text editor and chat features.
 
 Test Case ID: 
------------

Test Case Name: Create Chat Session<br />
Designed By: Wilson Zhu<br />
Executed By: Wilson Zhu<br />
Priority: High<br />
Short Description: Test the ability to create a new chat session<br />
Pre-Conditions:<br />
 *The user must be already logged in to DuoMonkeyEditor<br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click 'Chat Room' button| |A drop down list appears with 'Creat Session' button| |
|2 |Click 'Create Session' button| |A pop up box will appear for user to input session name and password| |
|3 |Type in session name and password|'session name' 'password'|A text editor appears on the left and chat room on right with 'Invite' and 'In room' drop down buttons| |

Post-Conditions:<br />
 *A new chat session has been created<br />
 *The user is now in a chat session by himself<br />
 
 Test Case ID: 
------------
Test Case Name: Join an existing chat session with the right password<br />
Designed By: Kevin Elizabeth<br />
Executed By: Kevin Elizabeth<br />
Priority: High<br />
Short Description: Test the ability to join a existing chat session  <br />
Pre-Conditions:<br />
 *The user must be already logged in to DuoMonkeyEditor<br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click 'Chat Room' button| |A drop down list appears with 'Creat Session' button| |
|2 |Click an existing seesion name from list| |A pop up box 'Join a Session' will appear for user to input session password| |
|3 |Type in session password then hit 'Enter'|'password'|A text editor appears on the left with previous work displayed and chat room on right with previously messages displayed| |

Post-Conditions:<br />
 *The user is now in a already existing chat session<br />
 
 Test Case ID: 
------------
Test Case Name: Join an existing chat session with the wrong password<br />
Designed By: Kevin Elizabeth<br />
Executed By: Kevin Elizabeth<br />
Priority: High<br />
Short Description: Test the ability to join a existing chat session  <br />
Pre-conditions: <br />
 *The user must be already logged in to DuoMonkeyEditor<br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click 'Chat Room' button| |A drop down list appears with 'Creat Session' button| |
|2 |Click an existing seesion name from list| |A pop up box 'Join a Session' will appear for user to input session password| |
|3 |Type in session password then hit 'Enter'|'wrong password'|The pop up box 'Join a Session' disappears|after inputing wrong password, we want a pop or alert box to appear to say 'Wrong Password'|

Post-Conditions:<br />
 *The user did not successfully join an exisitng chat session<br />

Test Case ID: 
------------
Test Case Name: Using text editor in an existing chat session<br />
Designed By: Kevin Elizabeth<br />
Executed By: Kevin Elizabeth<br />
Priority: High<br />
Short Description: Test the ability to type in a text editor in a chat session  <br />
Pre-Condition:  <br\>
 *The user must be already logged in to DuoMonkeyEditor<br />
 *The user must be logged in to a session.<br />

|Step |Action                   |Sample Input Data            |Expected Outcomes   |Comment                 |
|-----|-------------------------|-----------------------------|--------------------|------------------------|
|1 |Click inside the text editor| |The cursor flashes inside the text editor| |
|2 |Begin typing|'hello world'|on the text editor "hello world" should be displayed| |
|3 |highlight text with mouse| |The selected text is highlighted on both users' screens| |


Post-Conditions:
