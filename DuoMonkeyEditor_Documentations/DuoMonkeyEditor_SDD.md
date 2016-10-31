Software Design Document for DuoMonkeyEditor (version 1.0 approved)
===================================================================
Created by Aaron Dupont, Blake Allen, Jason Lee, Kevin Elizabeth, Wilson Zhu

Table of Contents
=================
**NOTE: Use Ctrl-F to nagivate the document**
* Introduction
* Main System Architecture
* Sub-Systems Architecture
* Rational Architectural Choices
* Development View
* Physical View
* Database View
* Work-Assignment View
* Element Catalog
* User Interfaces

Revision History
================
| Name        | Date      | Reason For Changes | Version |
| ----------- |:---------:| ------------------ | ------- |
| Aaron Dupont| 10/26/16  | Creation, Intro    |1.0      |
| Wilson Zhu  | 10/28/16  | Intro              |1.0      |
| Jason Lee   | 10/30/16  | Physical View      |1.0      |

Introduction
============
Purpose
-------
The purpose of this Software Design Document (SDD) is to describe how the DuoMonkeyEditor will be designed and implemented. The document should provide enough information to aid in the development process of the web application.
  
Intended Audience
-----------------
The DuoMonkeyEditor is a real-time collaborative editor that is intended for software developers that are performing pair programming. Although this concept of a real-time collaborative editor is not new, the DuoMonkeyEditor aims to be simple and easy to use, requiring only the user's existing Google account.

Scope
-----
The web application contains two major components that it will function with, the text editor and the messaging system. The user's interaction with the two components will be synced to the database, providing the real-time display of information between the users. This document will cover the architectural structure of each component as well as the overall structure of the application itself.
  
Overview
--------
The document will cover the following areas:
  * Main System Architecture (Logical View): Provides a description and graphical representation of the Main System and its relation to the application
  * Sub-Systems Architecture: Provides a description and graphical representation of each sub-system for DuoMonkeyEditor
  * Rational For Each Architectural Choice: Gives a deeper look into the decision making process of the design of each sub-system
  * Development View: Provides the layout and organization of DuoMonkeyEditor
  * Physical View: Provides the physical layout of the DuoMonkeyEditor
  * Database View: Discusses data models and database(s) that are used in DuoMonkeyEditor
  * Work-Assignment View: Provides a description of tasks and which developer has been assigned to complete it
  * Element Catalog: Lists all symbols and definitions, used in this document, for reader's clarity
  * User Interfaces: Provides a description and visual aid of the graphical user interface (GUI) for DuoMonkeyEditor
  

Main System Architecture
========================
General System Overview
-----------------------
    The DuoMonkeyEditor Architectural Diagram:
    +----------------------------------------+
    |           Front-end (Website)          |
    +----------------------------------------+
    +-----------------+   +------------------+
    |   Text Editor   |   | Messaging System |
    +-----------------+   +------------------+
    +----------------------------------------+
    |            Back-end (Server)           |
    +----------------------------------------+

<<<<<<< HEAD
The DuoMonkeyEditor is composed of 3 major layers. The first layer is the website itself, which is the graphical user interface that users will interact with. The second layer is application layer that is composed of the text editor and the messaging system, the user's interaction with the website/GUI will directly affect the application. The final layer is the server that the application will communicate with in order to sync the data across the instances of the application (only between communicating users).
=======
The DuoMonkeyEditor is composed of 3 major layers. The first layer is the website itself, which is the graphical user interface that users will interact with. The second layer is application layer that is composed of the text editor and the messaging system, the user's interaction with the website/GUI will directly affect the application. The final layer is the server that the application will communicate will in order to sync the data across the instances of the application (only between communicating users).
>>>>>>> master

Application Use Case
--------------------
          User                        DuoMonkeyEditor application
          /  \ /| |'-.         +---------------------------------------+
         .\__/ || |   |   -----|-------------------Login               |
      _ /  `._ \|_|_.-'   -----|----Create Session---------+<includes> |
     | /  \__.`=._) (_    -----|----Join Session-----------|<includes> |
     |/ ._/  |"""""""""|       |                    Inquire Password   |
     |'.  `\ |         |       |               <includes>              |
     ;"""/ / |         |  -----|-------Message--------\                |
      ) /_/| |.-------.|  -----|----Edit-------------Update            |
     '  `-`' "         "       |           <includes>                  |
                               +---------------------------------------+

When using the DuoMonkeyEditor, the user can do 5 things with the application. In order to use the application, the user needs to log in using their Google account. Upon logging in the application, the user then has two options, creating or joining a session. Whether the user chooses to create a new session or join an existing session, they are required to input the password associated with the session. Once in, the user can either edit code on the text editor or message using the messaging system, which is continuously updated with the database.

Sub-Systems Architecture
========================
Text Editor
-----------
    input from website ----> Back end ----> display on database

Messaging System
----------------
    input from website ----> back end ------> display on database

Rational For Each Architectural Choice
======================================
Text Editor
-----------
The architecture of the text editor was decided upon the disovery of firepad. Since firepad is able to connect to our back-end environment, firebase, it is imperative that the architecture must be 
Messaging System
----------------

# Development View
# Physical View
![PhysicalView](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Image/PhysicalView.PNG)
# Database View

Work-Assignment View
====================
It is in the best interest of the reader to illustrate the Work-Assignment View in descriptive text rather than visual representation. While DuoMonkeyEditor will be developed equally by each team member, please see the following task list that lists each members main focus:
*Front End
..*Aaron Dupont: CSS and design, Documentation
*Text Editor
..*Blake Allen: Main feature implementation
..*Jason Lee: Feature enhancement (font variations, highlighting) 
*Messaging System
..*Kevin Elizabeth: Feature enhancement 
*Back End
..*Wilson Zhu: Establishing connections between firebase and firepad/firechat, Creation of all subsystems

# Element Catalog
Physical View      
-------------
|Symbol                                                                                                                   |Description               |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------|
|![TextEditor](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Image/Optimized-textEditor.jpg)|Represents DuoMonkeyEditor|
|![Server](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Image/Optimized-Server.jpg)	      |FireBase server by Google |
|![User](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Image/Optimized-User.jpeg)		      |User                      |
# User Interfaces

this is the sdd & it is due Wednesday, Nov. 2 at 11:55PM
