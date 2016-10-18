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
Purpose
-------
The final product of this software specification is a working website (v1.0) that involves a server (Firebase), computers (web browsers), and a web application

Document Convention
-------------------
TODO: Put something here

Intended Audience and Reading Suggestions
-----------------------------------------
The target audience of this software requirements specification is for those who are interested in the internal workings of the DuoMonkeyEditor product. This includes (but not limited to):
 * Developers
 * Users
 * Testers
 
The software requirements specification is formatted based on the IEEE Std 830-1998 where the readers can nagivate the document using the table of contents.

Product Scope
-------------
The goal of this product is to enable programmers working in pairs to communication and work together, where physical distance is not a factor. The product will involve:
 * A Firebase server that is hosted by Google, which will provide a way for host the web application without having to worry about the back-end development of the application. The server will also provide a way to authenticate users and real-time data synchronization
 * Web browsers, which is the only way of accessing the web application
 * The web application, which is the core of the product that will provide the main features of the product
 
References
----------
[Firebase Reference](https://firebase.google.com/docs/reference/js/)  
[Firechat Reference](https://firechat.firebaseapp.com/docs/)
[Firepad Reference](https://firepad.firebaseapp.com/docs/)
** NOTE: The web application will be derived from Firechat and Firepad (with modified functionalities) **


Overall Description
===================
