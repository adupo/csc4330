Software Design Document for DuoMonkeyEditor (version 1.0 approved)
===================================================================
Created by Aaron Dupont, Blake Allen, Jason Lee, Kevin Elizabeth, Wilson Zhu

Table of Contents
=================
1. Introduction
   1. Purpose
   2. Intended Audience
   3. Scope
   4. Overview
2. Main System Architecture
   1. General System Overview
   2. Application Use Case
3. Sub-Systems Architecture
   1. Text Editor Architecture
   2. Messaging System Architecture
4. Rational Architectural Choices
   1. Text Editor Rational
   2. Messaging System Rational
5. Development View
6. Physical View
7. Database View
8. Work-Assignment View
9. Element Catalog
   1. Application Use Case Diagram Catalog
   2. Development View Catalog
   3. Physical View Catalog
   4. Database View Catalog
10. User Interfaces
   1. Front-end (Website) Interface
   2. Text Editor Interface
   3. Messgaing System Interface

**NOTE: Use Ctrl-F to nagivate the document**

Revision History
================
| Name            | Date      | Reason For Changes              | Version |
| --------------- |:---------:| ------------------              | ------- |
| Aaron Dupont    | 10/26/16  | Creation, Intro                 |1.0      |
| Wilson Zhu      | 10/28/16  | Intro, Main System Architecture |1.0      |
| Jason Lee       | 10/30/16  | Physical View, Element Catalog  |1.0      |
| Aaron Dupont    | 11/01/16  | Work Assignment View            |1.0      |
| Kevin Elizabeth | 11/01/16  | Database View                   |1.0      |
| Wilson Zhu      | 11/01/16  | Sub-System Architecture         |1.0      |
| Aaron Dupont    | 11/02/16  | User Interface                  |1.0      |
| Blake Allen     | 11/02/16  | Rational, Development View      |1.0      |
| Kevin Elizabeth | 11/02/16  | Database View                   |1.0      |
| Aaron Dupont    | 11/02/16  | Proofread, Finishing Touches    |1.0      |

1. Introduction
===============
&nbsp;&nbsp;&nbsp;i. Purpose
----------------------------
The purpose of this Software Design Document (SDD) is to describe how the DuoMonkeyEditor Application will be designed and organized. The document provides enough information to aid in the discription of the software system. 
  
&nbsp;&nbsp;&nbsp;ii. Intended Audience
---------------------------------------
The DuoMonkeyEditor is a real-time collaborative editor that is intended for software developers that are performing pair programming. Although this concept of a real-time collaborative editor is not new, the DuoMonkeyEditor aims to be simple and easy to use, requiring only the user's existing Google account.

&nbsp;&nbsp;&nbsp;iii. Scope
----------------------------
The web application contains two major components that it will function with, the text editor and the messaging system. The user's interaction with the two components will be synced to the database, providing the real-time display of information between the users. This document will cover the architectural structure of each component as well as the overall structure of the application itself.
  
&nbsp;&nbsp;&nbsp;iv. Overview
------------------------------
The document will describe the following areas:
  * Main System Architecture (Logical View): Provides a description and graphical representation of the Main System and its relation to the application
  * Sub-Systems Architecture: Provides a description and graphical representation of each sub-system for DuoMonkeyEditor
  * Rational For Each Architectural Choice: Gives a deeper look into the decision making process of the design of each sub-system
  * Development View: Provides the layout and organization of DuoMonkeyEditor
  * Physical View: Provides the physical layout of the DuoMonkeyEditor
  * Database View: Discusses data models and database(s) that are used in DuoMonkeyEditor
  * Work-Assignment View: Provides a mapping of each developer to the application architecture
  * Element Catalog: Lists all symbols and definitions used in this document, for the reader's clarity
  * User Interfaces: Provides a description and visual aid of the graphical user interfaces (GUI) for DuoMonkeyEditor
  

2. Main System Architecture
========================
&nbsp;&nbsp;&nbsp;i. General System Overview
--------------------------------------------
![architectural design](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/architecture_diagram.png)

The DuoMonkeyEditor application is composed of 3 major layers. The first layer is the website itself, which is the graphical user interface that users will interact with.  The first layer is rendered using Javascript and Bootstrap as its framework. The second layer is the application layer and it is made up of the text editor and the messaging system, as well as all the dependencies of the application components (UnderscoreJS and jQuery). The user's interaction with the website/GUI will directly affect the application. The final layer is the server that the application will communicate with in order to sync the data across the instances of the application (only between communicating users).

&nbsp;&nbsp;&nbsp;ii. Application Use Case
------------------------------------------
![application use case](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/application_use_case.png)

When using the DuoMonkeyEditor, the user can do 5 things with the application. In order to use the application, the user needs to log in using their Google account. Upon logging in the application, the user then has two options, creating or joining a session. Whether the user chooses to create a new session or join an existing session, they are required to input the password associated with the session. Once in, the user can either edit code on the text editor or message using the messaging system.

3. Sub-Systems Architecture
===========================
&nbsp;&nbsp;&nbsp;i. Text Editor Architecture
---------------------------------------------
![text editor](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/texteditor.png)

The architectural design of the text editor is similar to other popular editors. The user is able to input text into the text area of the text editor as well as change the font properties and the format of the text. The input text can be either over a selected area of text or based on the cursor position in the document. 

![line data structure](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/line.png)

The basic data type in the text editor is a line, which is essentially a linked list that contains the character data and the formatting of the character. If the linked list exceeds the length of the text area, a new line is created.

&nbsp;&nbsp;&nbsp;ii. Messaging System Architecture
---------------------------------------------------
![chat](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/chat.png)

The architectural design of the messaging system is simply a basic chat application that allows the user to communicate with other users. The user would input their message and the message is sent to the server to be added in the message board, which is to be displayed to the user. This system is heavily based on Firechat (by Firebase; Google).

4. Rational For Each Architectural Choice
=========================================
&nbsp;&nbsp;&nbsp;i. Text Editor Rational
-----------------------------------------
The architectural design of the text editor is heavily based up Firepad, which is an open-source applcation that is hosted by Firebase (Google). This text editor will have similar functionality as many other text editors including copy, paste, and select. Our text editor will also be using a linked list based implementation. When researching how text editors were created, the most effecient and commonly found implementations used this method. As mostly JAVA programmers, we are all fimilar with linked lists and found this is the easist way to implement the text editor. 

&nbsp;&nbsp;&nbsp;ii. Messaging System Rational
-----------------------------------------------
The architectural design of the messaging system is based mostly on Firechat (by Firebase; Google),which is an open-source application. The idea for the messaging system was to be able to link two programmers together who may not be near each other or who may want to view the code on their own machine, and have them still be able to talk. When researching the methods of creating a "real-time" messaging system, we kept this main idea in mind. A common approach to this architecture design si to have a database implementation, where text entered would be sent to a database and then displayed from that database to a recievers terminal. Taking advantage of the open source Firechat, our application uses FireBase for handling all the posts/recieves in the messaging system.

5. Development View
================
![development view](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/Development_View.png)

The DuoMonkeyEditor project will be using mostly html,js,css, and json files. The directory structure is shown above. NOTE: All boxes that are orange are directories and the grey boxs are source files.
The first and main directory is called DuoMonkeyEditor. It contains the directories for the css (style) and javascript (scripts) for the application. This directory also contains the main html and an icon that will be shown in the browser. 
The next directory is called style. In this directory the bulk of the css for the project is stored here.
In the next directory, called scripts, we store all the js files and one last directory called text.
In the last directory, called text, we have all files relating to the text editor portion of the project. 

6. Physical View
=============
![physical view](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/physical.PNG)

A user uses the web application DuoMonkeyEditor. The web application then sends input to a web server which in return delivers the text to the user's partner. The user's partner sees the output of what the user typed and sends any edits to the web application, through the server, to be updated.

7. Database View
=============
![database view](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/ER_Diagram.png)

The above graphical representation of the database for DuoMonkeyEditor represents the entities, and their attributes, that will be stored through FireBase. 

8. Work-Assignment View
====================
The following image is a graphical representation of the work assignment for DuoMonkeyEditor and how each team member maps to the architecture of the project.
![work assignment](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/architecture_diagram_work_assignment.png)

* Front-end (Website): Jason Lee, Kevin Elizabeth
* Application:
  * Text Editor:
    * UI: Blake Allen
    * Text Editor Functionality: Wilson Zhu
  * Messaging System:
    * UI: Aaron Dupont
    * Chat Functionality: Wilson Zhu
* The Back-end (Server): Wilson Zhu

9. Element Catalog
===============

&nbsp;&nbsp;&nbsp;i. Application Use Case Diagram Catalog
---------------------------------------------------------
| Symbol         | Description          |
| ------         | -----------          |
| ![actor] (https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/UseCase_Actor.png)  | Actor  |
| Green Oval     | Use Case             |
| Grey Rectangle | Application System   |
| Grey Arrow     | Association          |

&nbsp;&nbsp;&nbsp;ii. Development View Catalog
------------------------
| Symbol | Description |
| ------ | ----------- |
| Orange Rectangle | Represents a Directory   |
| Grey Rectangle   | Represents a Source File |
| Arrow            | Represents Inheritance   |

&nbsp;&nbsp;&nbsp;iii. Physical View Catalog  
-------------------------------------------
|Symbol                       |Description               |
|-----------------------------|--------------------------|
|![application](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/application.jpg)|represents the DuoMonkeyEditor application|
|![server](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/server.jpg)	      |represents the Firebase server|
|![user](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/user.jpeg)		        |represents the user|

&nbsp;&nbsp;&nbsp;iv. Database View Catalog
------------------------------------------
| Symbol                       | Description |
| -------                      | ----------- |
| ![Entity](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/Rectangle.png)    | Entity      |
| ![Relationship](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/Diamond.png)     | Relationship |
| ![Attribute](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/Oval.png)      | Attribute |
| ![OneToOne](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/oneToOneRelationship.png)| One to One Relationship |
| ![OneToMany](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/oneToManyRelationship.png)| One to Many Relationship |
| ![ManyToMany](https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/manyToManyRelationship.png)| Many to Many Relationship |

10. User Interfaces
===============
Below is the graphical user interface for DuoMonkeyEditor and a short description of how they map to the architecture.

&nbsp;&nbsp;&nbsp;i. Front-end (Website) Interface
--------------------------------------------------
<img src="https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/MainScreen.png" alt="Website" height="300" width="450" />
<img src="https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/DuoMonkeyEditor_Login.png" alt="Website" height="300" width="250" /> <br />

This is the mock up of the graphical user interface for the DuoMonkeyEditor website. Users will be presented with this interface upon arriving at the website.
* Allows logging in by clicking "Get Started" which will open the Google login screen (pictured above).
* Allows access to the application.

&nbsp;&nbsp;&nbsp;ii. Text Editor Interface
-------------------------------------------
<img src="https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/FirePad_Mockup.png" alt="Website" height="300" width="550" /> <br />

This is the mock up of the graphical user interface for the DuoMonkeyEditor text editor. Users will be presented with this interface after inputing their Google account in the screen above.
* Allows input and modification of text.
* Allows font changes to text. 
* This is the main feature of the GUI.

&nbsp;&nbsp;&nbsp;iii. Messaging System Interface
-------------------------------------------------
<img src="https://github.com/adupo/csc4330/blob/master/DuoMonkeyEditor_Documentations/Assets/ChatRoom.png" alt="Website" height="450" width="400" /> <br />

This is the mock up of the graphical user interface for the DuoMonkeyEditor messaging system. Users will be presented with this interface alongside the text editor interface.
* Allows sending and receiving messages.

