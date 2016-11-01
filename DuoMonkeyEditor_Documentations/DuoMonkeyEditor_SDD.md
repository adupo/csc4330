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

The DuoMonkeyEditor is composed of 3 major layers. The first layer is the website itself, which is the graphical user interface that users will interact with. The second layer is application layer that is composed of the text editor and the messaging system, the user's interaction with the website/GUI will directly affect the application. The final layer is the server that the application will communicate with in order to sync the data across the instances of the application (only between communicating users).

Application Use Case
--------------------
![application use case](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/application_use_case.png)

When using the DuoMonkeyEditor, the user can do 5 things with the application. In order to use the application, the user needs to log in using their Google account. Upon logging in the application, the user then has two options, creating or joining a session. Whether the user chooses to create a new session or join an existing session, they are required to input the password associated with the session. Once in, the user can either edit code on the text editor or message using the messaging system, which is continuously updated with the database.

Sub-Systems Architecture
========================
Text Editor
-----------
![text editor](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/text_editor.png)

The architectural design of the text editor is like every other text editor. The user is able to input text into the text editor (the text area) as well as changing the font properties and the format of the text. The input text can be either over a selected area of text or based on the cursor position in the document. This system is heavily based on Firepad (by Firebase; Google).

Messaging System
----------------
![chat](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/chat.png)

The architectural design of the messaging system is simply a basic chat application that allows the user to communicate with other users. The user would input their message and the message is sent to the server to be added in the message board, which is to be displayed to the user. This system is heavily based on Firechat (by Firebase; Google).

Rational For Each Architectural Choice
======================================
Text Editor
-----------
The architectural design of the text editor is heavily based up Firepad, which is an open-source applcation that is hosted by Firebase (Google). The text editor functions operates like every other text editor and the integration with the Firebase server makes it easier to implement the text editor in the application.

Messaging System
----------------

Development View
================

Physical View
=============
![physical view](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/physical.PNG)

A user uses the web application DuoMonkeyEditor. The web application sends input to web server which then forwards the messages to the user's partner. The user's partner using DuoMonkeyEditor sees the output of what the user typed and sends any edits to the web application and throught the server to be updated.

Database View
=============
![DatabaseView]()

Work-Assignment View
====================
The following is the work assignment of the components of the DuoMonkeyEditor:
* The website (front-end): Jason Lee, Kevin Elizabeth
* The application:
  * Text Editor:
    * UI: Blake Allen
    * Text Editor Functions: Wilson Zhu
  * Messaging System:
    * UI: Aaron Dupont
    * Chat Functions: Wilson Zhu

Element Catalog
===============
Physical View Catalog  
---------------------
|Symbol                                                                                                                   |Description               |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------|
|![application](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/application.jpg)|Represents DuoMonkeyEditor|
|![server](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/server.jpg)	      |FireBase server by Google |
|![user](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/user.jpeg)		        |User                      |

User Interfaces
===============
