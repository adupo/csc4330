Software Requirements Specification for DuoMonkeyEditor (version 1.0 approved)
==============================================================================
Created by Aaron Dupont, Blake Allen, Jason Lee, Kevin Elizabeth, Wilson Zhu

Table of Contents
=================
** NOTE: Use Ctrl-F to nagivate the document **
* Revision History  
* Introduction  
  * Purpose  
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
  *	User Login
  *	Chat
  * Text Editor
*	Other Nonfunctional Requirements
  *	Performance Requirements  
  *	Security Requirements  
  *	Software Quality Attributes  
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
This section give the entire overview of the system that the DuoMonkeyEditor is composed of as well as the interactions with other applications or systems.

Product Perspective
-------------------
The DuoMonkeyEditor is aim to be a workaround or replacement to current text editors. The web application is composed of two components: the webpage and the server. The webpage (front-end) will serve the main way for pair programmers to use the application, any interactions with the webpage is handled by the server (back-end).

                          [user] ----(interacts)----> [webpage] ----(passes user input)----> [server]

Product Functions
-----------------
The DuoMonkeyEditor will have the following major functions:
 * login: logs the user into the web application (DuoMonkeyEditor)
 * create room: creates the chat room and the text editor (there will also be a password associated with it)
 * join room: joins an existing chat room and text editor
 * message: creates and send messages in the chat system
 * edit: editing contents on the text editor

User Classes and Characteristics
--------------------------------
The DuoMonkeyEditor is a web application for programmers doing pair programming. The desired users for this application are programmers who understanding how to use a basic chat system.

Operating Environment
---------------------
The DuoMonkeyEditor will operate on major web browsers (ie: Chrome, Firefox, Internet Explorer, etc.) on PCs and Macs. The software is not intended for mobile devices (smartphones).

Design and Implementation Contraints
------------------------------------
The web application is only intended for web browsers on PCs, Macs, and Linux. Although the application may work on the mobile platform, it is not the intended environment for the application.

User Documentation
------------------
In order for users to fully utilize the DuoMonkeyEditor application, users must have an existing Google account. Once logged in, the user would have two options: create a session or join a session. By either creating or joining a session, users are able to connect with their partners and communicate with each other using the chat system and working on their programming task using the text editor.

Assumptions and Dependencies
----------------------------
It is assumed that the users has internet connection and a Google account. Users should be able to nagivate the webpage with no problem and use a basic text editor and chat system.

External Interface Requirements
===============================
This section states the required characteristics at a point/region of connection of the system to the outside world.

User Interfaces
---------------
Upon logging into the application, users will face a lobby that will give them two options; creating a session or joining an existing session in the form of buttons. Upon entering a session, the user will be faced with a text editor to the left-side of the user's screen and the chat system to the right-side of the screen.

Hardware Interfaces
-------------------
The DuoMonkeyEditor application is supported on only Macs and PCs with web browsers (ie: Chrome, Firefox, Internet Explorer, etc.). Users will input their information using their comptuters and the server will process the inputted information.

Software Interfaces
-------------------
The DuoMonkeyEditor application will utilize the Firebase server as well as their APIs, and work with Windows, Mac, and Linux environments.

Communication Interfaces
------------------------
The DuoMonkeyEditor will rquire the users to login with their Google account and the communication standards the application uses will be HTTP. All security, data, and synchronization mechanisms will be handled by the Firebase server.

System Features
===============
This section will describe all the features that the DuoMonkeyEditor will have.

Login
-----
Authenticates users using their Google account, and allow user access to other features  
Priority: Very high  
Response Sequence:  

    user ---(clicks 'login')---> webpage ---(request user info)---> user ---(inputs info)---> webpage ---(passes user info)---> server
    
Function Requirements:  
 * Login button: Used to initiate login action
 * Email input field: Will take in Google email account
 * Password input field: Will take in the user's Google password
 * Authenication: Will check user's inputted Google account and password; will throw an error if incorrect/empty
 
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

Text Editor
-----------
The text editor that will be used by the users for pair programming, synchronized between the users by the server
Priority: Low
Response Sequence:  
** NOTE: The text editor will be instantiate when the user creates a chat room **

    server ---(instantiate chat room and text editor)---> webpage ---(displays)---> user
    
Other Nonfunctional Requirements
================================
This section describes the characteristics of the DuoMonkeyEditor.

Performance Requirements
------------------------
The application should not lag.

Security Requirements
---------------------
The users' Google account privacy and security are taken care by the Firebase server (Google itself)
 
Software Quality Attributes
---------------------------
The DuoMonkeyEditor is made based off of intuitive ease of use for users.

Appendix
========
Additional information

Appendix A: Glossary
--------------------


Appendix B: Analysis Models
---------------------------


Appendix C: To Be Determined List
---------------------------------
