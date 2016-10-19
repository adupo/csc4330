Software Requirements Specification for DuoMonkeyEditor (version 1.0 approved)
==============================================================================
Created by Aaron Dupont, Wilson Zhu

Table of Contents
=================
** NOTE: Use Ctrl-F to nagivate the document **
* Revision History  
* Introduction  
  * Purpose  
  *	Document Conventions  
  *	Intended Audience and Reading Suggestions  
  *	Product Scope  
  *	References  
*	Overall Description
  *	Product Perspective
  *	Product Functions
  *	User Classes and Characteristics
  *	Operating Environment
  *	Design and Implementation Constraints
  *	User Documentation
  *	Assumptions and Dependencies
*	External Interface Requirements
  *	User Interfaces  
  *	Hardware Interfaces  
  *	Software Interfaces  
  *	Communications Interfaces  
*	System Features
  *	System Feature 1  
  *	System Feature 2 (and so on)  
*	Other Nonfunctional Requirements
  *	Performance Requirements  
  *	Safety Requirements  
  *	Security Requirements  
  *	Software Quality Attributes  
  *	Business Rules  
*	Other Requirements
  * Appendix A: Glossary  
  * Appendix B: Analysis Models  
  * Appendix C: To Be Determined List  

Revision History
================
TODO: Put something here

Introduction
============
This section gives a brief overview of everything about the DuoMonkeyEditor web application

Purpose
-------
The purpose of this document is to give a detailed description of all the requirements for the DuoMonkeyEditor web application. The document also describes may other aspects of the application such as the design constraints and interfaces.

Document Convention
-------------------
TODO: Put terms that readers may not understand

Intended Audience and Reading Suggestions
-----------------------------------------
The target audience of this software requirements specification is for those who are interested in the workings of the DuoMonkeyEditor web application. This includes (but not limited to):
 * Developers
 * Users
 * Testers
 
The software requirements specification is formatted based on the IEEE Std 830-1998 where the readers can nagivate the document using the table of contents.

Product Scope
-------------
DuoMonkeyEditor is a web application that aims to enable programmers working in pairs to communication and work together, where physical distance is not a factor. Users using the application will be able to communicate with their partners using the integrated chat system that is placed with the real-time data synchronizing text editor. The product will involve the following:
 * A Firebase server that is hosted by Google, which will provide a way for host the web application without having to worry about the back-end development of the application. The server will also provide a way to authenticate users and real-time data synchronization
 * Web browsers, which is the only way of accessing the web application
 * The web application, which is the core of the product that will provide the main features of the product
 
References
----------
** NOTE: The web application will be derived from Firechat and Firepad (with modified functionalities) **  
[Firebase Reference](https://firebase.google.com/docs/reference/js/)  
[Firechat Reference](https://firechat.firebaseapp.com/docs/)  
[Firepad Reference](https://firepad.firebaseapp.com/docs/)  

Overall Description
===================
This section gives the entire overview of the system that the DuoMonkeyEditor is composed of as well as the interactions with other applications or systems.

Product Perspective
-------------------
The DuoMonkeyEditor is designed to be a workaround or replacement to current text editors. The web application is composed of two components: the webpage and the server. The webpage (front-end) will serve the main way for pair programmers to use the application, any interactions with the webpage is handled by the server (back-end).

    [user] ---(interacts)---> [webpage] ---(passes user input)---> [server]

Product Functions
-----------------
The DuoMonkeyEditor will have the following major functions:
 * login: the main way of authenticating users, and allowing access to other major functions
 * create: 
 Insert "top level data flow diagram or object class diagram here"
 
User Classes and Characteristics
--------------------------------

Operating Environment
---------------------

Design and Implementation Constraints
-------------------------------------

User Documentation
------------------

Assumptions and Dependencies
----------------------------

External Interface Requirements
===============================
TODO: Put stuff here

User Interfaces
---------------
Users will click on "Login with Google" on the front page.....(More to come...)

Hardware Interfaces
-------------------
An electronic device that has access to Internet, has virtual or physical keyboard for typing, and a display screen. 

Software Interfaces
-------------------
DuoMonkeyEditor can be accessed by any devices that can run the latest version web browser applications including 

	Chrome(54.0.2840.59), Microsoft Edge(38.14393.0.0) , Mozilla Firefox(49.0.1), or Safari(10.0). 

Devices that access DuoMonkeyEditor includes any desktop/laptop computer or smaller devices including tablets and mobile devices that runs on Mac OS, iOS, Windows, or Android operating systems up to the latest version.

Communications Interfaces
-------------------------
A working Gmail account will be needed to access DuoMonkeyEditor, and the latest available web browser application as well. All users of DuoMonkeyEditor must also have access to Internet, either Wi-Fi or ethernet.

System Features
===============

User Login
----------
Authenticates users using their Google account, and allow user access to other features  
Priority: Very high  
Response Sequence:  

    user ---(clicks 'login')---> webpage ---(request user info)---> user ---(inputs info)---> webpage ---(passes user info)---> server ---(adds user)
    
Function Requirements:  
 * Login button: To initiate login action
 * Email input field: Will take in Google email account
 * Password input field: Will take in the user's Google password
 * Authenication: Checks user's inputted Google account and password; will throw error if fields are incorrect/empty
 
Chat
----
The main way for users to communicate with their partner  
Priority: High
Response Sequence:

    user ---(creates chat room)---> webpage ---(calls)---> server ---(instantiate chat room)---> webpage ---(displays chat room)---> user
    
    user ---(joins chat room; inputs password)---> webpage ---(calls)---> server ---(validates; add user to room)---> webpage ---(displays chat room) ---> user

Function Requirements:
 * Create Room button: To instantiate a chat room (also ask for a password for the room)
 * Join Room button: To join a chat room (user must also input the correct password)
 * The maximum number of users allowed in the chat room is two (for pair programming)
