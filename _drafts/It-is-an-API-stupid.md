<center><b>or: It's APIs All the Way Down</b></center>

Syst

You can look at a software system 


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
-> a Class is the smallest API (you work with / on)
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
eyJoaXN0b3J5IjpbMjA0NDc4MTA0LC0xNTQ4NTU1MzM1LC0yMD
AwNzU4OTA5LC0xMjE2NzU3NTQxLDE1OTAwOTQwMTAsMTY0Mzkx
ODk0OCwtMTY2MDUwMzMxMiwtMjQ4NTA4NjU3LDIxMTM1NjM2Mz
ksLTE5OTkzMTg3NzIsLTIwMjk1MzU4NTMsLTExMTc5NTg4ODcs
NDA3ODI2Nzk3LDIxMDk3Mjg0OTksMTE0NTY2MjkwM119
-->