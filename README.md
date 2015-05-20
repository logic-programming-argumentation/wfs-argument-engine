# WFS Argument Engine
The WFS argument engine build arguments based on the notion of an argument under  the Well-Founded semantics and Stable semantics inferences, allowing us to identify arguments with stratified programs as support, even when the input for the argument engine is a non-stratified program.

The underlying formalisms of the WFS argument engine are introduced in the paper: **Semantic-based Construction of Arguments: an Answer Set Programming Approach**, [Esteban Guerrero](http://www8.cs.umu.se/~esteban/), [Juan Carlos Nieves](http://www8.cs.umu.se/~jcnieves/) and [Helena Lindgren](http://www8.cs.umu.se/~helena/), 2015. Semantic-based Construction of Arguments: an Answer Set Programming Approach. International Journal of Approximate Reasoning.

#Short Description:

![Argument Engine. Figure 1](http://www8.cs.umu.se/~esteban/img/argengineworkflow.png) 

The implementation of our argumentation engine is based on Java, using [InterProlog](http://interprolog.com/) as middleware for calling the [XSB](http://www.xsb.com/) solver, as shown in Figure 1. Our WFS argument engine captures an extended logic program using Prolog code as input. By considering a program as a directed graph, the argument engine performs a graph analysis checking connected components. Relevant rules for a particular atom are obtained by obtaining their subsets of connected atoms and generating all their possible subsets. The WFS analysis is performed by using InterProlog function calls which transforming XSB procedures to Java objects and conversely. Data regarding to the graph analysis, the evaluated support for a given conclusion is stored in an embedded database. The integration of support and conclusion for building the argument is one of the last steps of the workflow, composing the argument, storing it in the database and finally generating the user interface for displaying. 

The argument engine exports the built arguments in a JSON format, an implementation exporting arguments in an argument interchange format will be part of future versions of our argument engine. More information about the WFS argumentation engine, as well as installation manuals and examples, are available in  [http://www8.cs.umu.se/~esteban/wfsArgEngine](http://www8.cs.umu.se/~esteban/wfsArgEngine).
