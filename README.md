DuoMonkeyEditor
===============
This repository will hold our group project for CSC 4330

Members include
---------------
1. Aaron Dupont
2. Blake Allen
3. Jason Lee
4. Kevin Elizabeth
5. Wilson Zhu


Work Done
---------
* Created the GitHub repo and added all members of the team to it.
* Created Project Management document (Oct. 11)
* Successfully deployed website (with working chat system)

Work to be Done
---------------
* Work on the application
 * As of right now, the application is composed of two major sections as well as two dependencies that we do not have to worry about.
 * The two components are the chat itself, which contains the functionality of the chat system and the chatUI that binds the chat function to the UI. The way it is currently working is as follows:
    * User clicks the login button which calls the login function that is defined in the index.html (user inputs their info)
    * Then the authStateChanged function will execute when it detects that the user has sucessfully logged in, which then calls the initApp function
    * The initApp function will then retrieve all the necessary parameters (eg. Database reference) for calling the chatUI, which in turns calls the chat itself (that is defined in the js file itself)
 * The components and the dependencies are all placed together in a js file to reduce the server load time to retrieve them
 * The js file will contain the TODO list that we need to work on:
   * The first major task is to have the chat require a password to enter (these must be defined in the room attributes and defined in the createRoom and joinRoom function) and modify the UI accordingly.
