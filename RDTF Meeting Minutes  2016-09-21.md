
---
title: "R Documentation Task Force Meeting Notes"
date: "2016-09-21"
---

# RDTF Meeting Notes 
## *2016-09-21*

## Links
* [YouTube Stream](http://youtu.be/KmZZGXyOuSI)

## Agenda
* Introductions  
* Guiding principles of the working group.  
	 + The principle of consensus
		 - Maintainability of the project
		 - Complexity Amount of work to implement
    + Resolution of decisions through empirical evidence  
    + Consulting outside opinion  
    + Implementer has the final say.
* Discussion of Aims with outlining specific goals, issues, and scope.  
    + We will abstract, document and implement in R a representation 
       for documentation of R objects; functions, classes, datasets, etcetera.  
    + The Task Force will make recommendations for methods, in addition 
       to the Rd format, to be supported for converting into internal 
       documentation objects. Recommendations will also be made
       for supported formats to convert to directly.  
    + We will implement the abstraction of documentation according
        to the results of Aim 1. According to the recommendations 
       resulting from aim 2, we will implement methods to convert from 
       supported sources of documentation to newly define documentation 
       objects, and from the internal representation to the supported output 
       formats. 
* Review of Current State 
    + Rd Format 
    + Roxygen 
    + inlinedocs/lint 

## Attendees
* Andrew
* Sarah 
* Martin
* Duncan
* Kirill

##Minutes

###Discussion of principles

* Duncan Proposed a plugin system.
* Considerations for gaining consensus 
    + Complexity Involved.
    + Maintainability
    + R Core change?
*  Added *"Person implementing has the final say"* to the principles of the group.

###Discussion of Aims

* Duncan brought up the issue that it is currently possible to have a different web pages on different systems, and that unix users should be able to see what Windows or Mac users see and vice versa.  There should be one documentation to rule them all.
* Andrew's counterpoint: the system is valuing flexibility over rigidity. Conditionally showing documentation is fundamental to that.  
	+ The documentation should still be present and accessible, but can be flagged as system specific.  In output like html, this could be not displayed or collapsed but still available. 
* Sarah brought up the point that it would be nice to be able to ask for the different components desired such as examples only in the requested documentation.
* Connection to Vignettes and Literate programming
	+ Documentation could be contained in the vignette with a parser that extracts the relevant information.
	+ Documentation could be in comments in the code chunks that are then extracted and optionally placed in the vignette.
	+ The flexibility of the system should be 

### Review of Current State

* Review of Current State 
    + Rd Format 
	    - Parse tree format currently (created approx. 2005)
	    - internal format is essentially a list of lists of lists of ...
	    - Not documented, and not meant to be in "user-land"
	    - Holds equal syntax and structure tags
    + Roxygen
	    - Now supports a plugin system.
	    - Now supports inline comments


## Scratch
* Martin and Andrew mentioned concerns about the trend of packages to replace in package documentation with website based documentation
* Duncan mentioned that one way of keeping maintaining the principle of proximity is to create  links from documentation to code and vice versa.  Something that could be achieved in RStudio or Emacs.


> Written with [StackEdit](https://stackedit.io/).