<center><b>or: It's APIs All the Way Down</b></center>

# A few Words on Software Architecture
> Ἐν ἀρχῇ ἦν ὁ λόγος.

Architecture isn't something that just happens. Architecture can't be an afterthought. Architecture isn't just the packaging of functionality. Architecture is an emergent property of a well designed system. You can make many decisions during the design process that influence its flavor but none of those change its substance. 
Architecture is an expression of the constraints that are defined by what we mean by a "well designed system". While that seems tautological at first glance, it isn't. The design of a system is driven by a set of properties we want the system to exhibit. The architecture is the way those properties are realized in the system. It is the difference between the what and the how. Therefore a well designed system is a system that expresses the right properties for its use cases while a well implemented architecture fulfills those properties.

While the set of properties a system should exhibit differs violently on a case to case basis, some are widely understood as being the lowest common denominator:
- correctness (duh!)
- extensibility
- maintainability

Other desirable properties might be:
- security (this one should really be in the core group, but it rarely is)
- scalability
- reusability
- durability

High performance and low operational or building costs can also be thrown into the mix, among others.

Creating a system that embodies the three core properties can be achieved in a number of ways, depending on the paradigms you are employing in building it, but they are always driven by the same principles.

- _Correctness_ is best accomplished by creating readable, independent, atomic and therefore testable functions.
- _Extensibility_ is achieved by decoupling logically independent functionality and providing well defined communication channels in between.
- _Maintainability_ is heavily driven by the other two and mainly constrains how those should be implemented. Or to put it another way: _Maintainability_ is a measure on how well the relevant driving principles are enforced throughout the system.

The principles identified above comunicate a clear possible solution: create independent bundles of logically interconnected, minimal funtionality that expose well defined cominocation channels. 




Is Software Architecture an emergent property?

You can look at a software system from a variety of perspectives and distances.


Diablo Anecdote
https://medium.com/@berniedurfee/never-trust-a-client-not-even-your-own-2de342723674

https://www.raphkoster.com/games/laws-of-online-world-design/the-laws-of-online-world-design/
<image source="http://rosettacode.org/mw/images/d/d7/Fractal_tree.svg" />


https://static.googleusercontent.com/media/research.google.com/de//pubs/archive/32713.pdf


slice and dice

what is a system


level:
- independent systems ???
- interdependent systems (app / db / auth)  ???
- components 
- packages
- class

proprties of good apis
- statelessness / decoupled
- consistency
- clear parameter / also parameter order
- clear names
- short parameter lists
- wrapper for complex operations


software architecture as api design


Everything is an API
-> a Class is the smallest API (you workl with / on)
-- Statelessness, Closed, The programmer is the enemy



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
eyJoaXN0b3J5IjpbMTY0NTc4OTEwNCwyMTA0MTg0NjA1LC0zMz
E3MTE1NjcsMjA4MDU5MDg1OCw1OTk2MTM2NTksLTIwNjgyNDY0
NiwzNzE4NTAyMzMsLTIxMjI2MTA2MjksLTEyODU5NDc0MDgsNj
Y4NzY0MTA2LDIxMzAyNDg3NTUsLTIwODk3OTYwMzgsLTIwMDkw
MDIwMCwxMzI5MzQ4MDI2LC0xMjA4NDU1MjI0LDY2MTY5MjAwNy
wyNzQwMDU0OTksMzI1ODA0OTcsLTgyNzUwOTgyMSwtMTQ0Nzcz
Mjg2OF19
-->