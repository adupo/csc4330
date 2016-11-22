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
