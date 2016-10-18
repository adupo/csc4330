Software Requirements Specification for DuoMonkeyEditor (version 1.0 approved)
==============================================================================
Created by Aaron Dupont, Blake Allen, Jason Lee, Kevin Elizabeth, Wilson Zhu

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
This section give the entire overview of the system that the DuoMonkeyEditor is composed of as well as the interactions with other applications or systems.

Product Perspective
-------------------
The DuoMonkeyEditor is composed of two components: the webpage and the Firebase server. The web
