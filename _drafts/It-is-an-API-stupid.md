---
title: It's an API Stupid 
tags:
- architecture
- programming
- object oriented design
- api design
---
<center><b>or: It's APIs All the Way Down</b></center>

The following is a brief summery of my views on software architecture. Those views are of course heavily influenced by others who have far more experience at this.  Nevertheless, I hope that I not only can do them justice 

# A very few Words on Software Architecture
> Ἐν ἀρχῇ ἦν ὁ λόγος.

Architecture isn't something that just happens. Architecture can't be an afterthought. Architecture isn't just the packaging of functionality. Architecture is an emergent property of a well designed system. You can make many decisions during the design process influencing its flavor but none of those change its substance. 
Architecture is an expression of the constraints that are defined by what we mean by "well designed system". While that seems tautological at first glance, it isn't. The design of a system is driven by a set of properties we want the system to exhibit. The architecture is the way those properties are realized in the system. It is the difference between the what and the how. Therefore a well designed system is a system that expresses the right properties for its use cases while a well implemented architecture fulfills those properties.

## Extracting some Core Principles

While the set of properties a system should exhibit differs violently on a case to case basis, some are widely understood as being the lowest common denominator:
- correctness (duh!)
- extensibility
- maintainability

Other desirable properties might be:
- security (this one should really be in the core group, but it rarely is)
- scalability
- reusability
- durability

Performance, fault tolerance, and low operational or building costs can also be thrown into the mix, among others.

Creating a system that embodies the three core properties can be achieved in a number of ways, depending on the paradigms you are employing in building it, but they are always driven by the same principles.

- _Correctness_ is best accomplished by creating readable, independent, atomic and therefore testable functionality.
- _Extensibility_ is achieved by decoupling logically independent functionality and providing well defined communication channels in between.
- _Maintainability_ is heavily driven by the other two and mainly constrains how those should be implemented. Or to put it another way: _Maintainability_ is a measure on how well the relevant driving principles are enforced throughout the system.

## First Conclusions

The principles identified above guide us to possible solution: create independent bundles of logically interconnected, minimal functionality that expose well defined entry points. In other words: hide interrelated functionality behind a single API.

# Even fewer Words on Good API Design
>Never trust the client. The client is in the hands of the enemy.

Good API design is not easy. API design in itself is not more complicated than implementing a good architecture but while the architecture structures your code and is therefore mostly hidden from the outside observer, an API by it's very nature is completely exposed to the outside. The consequence is, that you can't refactor an API once it has been published because people might actually use it. After all that is the whole point. So you need to get it right the first time and getting something right the first time is hard.
There is a very informative talk by Joshua Bloch on the topic of good API design <a href="#f1">[1]</a> and I urge you to check it out. 
The Reader's Digest version is: an API should make sense, be easy to use and hard to misuse. 
Some of the implementation guidelines derived from this are:
- minimal functionality
- clear and consistent names
- short parameter lists
- consistent parameter order
- simple, fault tolerant return values
- consistent and transparent error handling
- hide implementation details

SUMMERY

I would like to extend that list:
- consistency: <- already there
- wrapper for complex operations
- statelessness / decoupled / atomic / transactional
- Statelessness, Closed, The programmer is the enemy


# Down the Rabbit Hole 

level:
- independent systems ???
- interdependent systems (app / db / auth)  ???
- components 
- packages
- class
- overloaded methods???

Everything is an API
-> a Class is the smallest API (you work with / on)

You can look at a software system from a variety of perspectives and distances.

# Somethings Owed
Process -> SOLID Principles
Maintainablillity -> What? How?

Diablo Anecdote
https://medium.com/@berniedurfee/never-trust-a-client-not-even-your-own-2de342723674

https://www.raphkoster.com/games/laws-of-online-world-design/the-laws-of-online-world-design/
<image source="http://rosettacode.org/mw/images/d/d7/Fractal_tree.svg" />





slice and dice

what is a system



software architecture as api design


# Footnotes
<a id="f1"></a>[1] Bloch, Joshua _How to Design a Good API and Why it Matters._ Google Tech Talks., 2007. <a href="https://www.youtube.com/watch?v=aAb7hSCtvGw">[Video]</a> <a href="https://static.googleusercontent.com/media/research.google.com/de//pubs/archive/32713.pdf">[Slides]</a>
# Further Reading



<svg xmlns="http://www.w3.org/2000/svg"   
 xmlns:xlink="http://www.w3.org/1999/xlink"  
 width="400" height="320">  
  <style type="text/css"><![CDATA[  
 line { stroke: black; stroke-width: .05; }  
 circle { fill: black; }  
 ]]></style>  
   
<defs>  
  <g id="stem"> <line x1="0" y1="0" x2="0" y2="-1"/> </g>  
   
  <g id="l0"><use xlink:href="#stem"/></g>  
  <!-- These are identical except for the id and href. -->  
  <g id="l1"> <use xlink:href="#l0" transform="translate(0, -1) rotate(-35) scale(.7)"/>  
              <use xlink:href="#l0" transform="translate(0, -1) rotate(+35) scale(.7)"/>  
              <use xlink:href="#stem"/></g>  
  <g id="l2"> <use xlink:href="#l1" transform="translate(0, -1) rotate(-35) scale(.7)"/>  
              <use xlink:href="#l1" transform="translate(0, -1) rotate(+35) scale(.7)"/>  
              <use xlink:href="#stem"/></g>  
  <g id="l3"> <use xlink:href="#l2" transform="translate(0, -1) rotate(-35) scale(.7)"/>  
              <use xlink:href="#l2" transform="translate(0, -1) rotate(+35) scale(.7)"/>  
              <use xlink:href="#stem"/></g>  
  <g id="l4"> <use xlink:href="#l3" transform="translate(0, -1) rotate(-35) scale(.7)"/>  
              <use xlink:href="#l3" transform="translate(0, -1) rotate(+35) scale(.7)"/>  
              <use xlink:href="#stem"/></g>  
  <g id="l5"> <use xlink:href="#l4" transform="translate(0, -1) rotate(-35) scale(.7)"/>  
              <use xlink:href="#l4" transform="translate(0, -1) rotate(+35) scale(.7)"/>  
              <use xlink:href="#stem"/></g>  
  <g id="l6"> <use xlink:href="#l5" transform="translate(0, -1) rotate(-35) scale(.7)"/>  
              <use xlink:href="#l5" transform="translate(0, -1) rotate(+35) scale(.7)"/>  
              <use xlink:href="#stem"/></g>  
  <g id="l7"> <use xlink:href="#l6" transform="translate(0, -1) rotate(-35) scale(.7)"/>  
              <use xlink:href="#l6" transform="translate(0, -1) rotate(+35) scale(.7)"/>  
              <use xlink:href="#stem"/></g>  
  <g id="l8"> <use xlink:href="#l7" transform="translate(0, -1) rotate(-35) scale(.7)"/>  
              <use xlink:href="#l7" transform="translate(0, -1) rotate(+35) scale(.7)"/>  
              <use xlink:href="#stem"/></g>  
  <g id="l9"> <use xlink:href="#l8" transform="translate(0, -1) rotate(-35) scale(.7)"/>  
              <use xlink:href="#l8" transform="translate(0, -1) rotate(+35) scale(.7)"/>  
              <use xlink:href="#stem"/></g>  
</defs>  
   
<g transform="translate(200, 320) scale(100)">  
  <use xlink:href="#l9"/>  
</g>  
   
</svg>



> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIxMzMwNzU2MzcsLTE4MDA2ODI1NjQsLT
E4Nzg0MTE3MTIsMzQ3NjE5ODI0LDIwMjkwMTMwOTgsLTEwMzMx
NTYwMjAsLTI3MTk4NDAyOCwxNjQxODE3MDI0LC0xNzk0MDExNj
k5LDE3NTE0MTUyMDUsLTIwNTkyODY3NzQsNDY2MTUwMTA4LC0y
NzU5NjA3OTUsMjAwNDU3OTk5MSwyMDg5Mzk5MDQwLDE1MTgyNz
A2ODQsLTg4OTQ3NzMzNywtMTkwMTA3MTE4NCwxNjI1NDQ0ODI0
LC0xMDA0OTYwMDE1XX0=
-->