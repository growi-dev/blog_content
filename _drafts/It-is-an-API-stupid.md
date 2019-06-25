<center><b>or: It's APIs All the Way Down</b></center>

Diablo Anecdote

https://www.raphkoster.com/games/laws-of-online-world-design/the-laws-of-online-world-design/
<image source="http://rosettacode.org/mw/images/d/d7/Fractal_tree.svg" />


https://static.googleusercontent.com/media/research.google.com/de//pubs/archive/32713.pdf

<canvas id="canvas" width="600" height="500"></canvas>  
   
<script type="text/javascript">  
var elem = document.getElementById('canvas');  
var context = elem.getContext('2d');  
   
context.fillStyle = '#C0C0C0';  
context.lineWidth = 1;  
   
var deg_to_rad = Math.PI / 180.0;  
var depth = 9;  
   
function drawLine(x1, y1, x2, y2, brightness){  
  context.moveTo(x1, y1);  
  context.lineTo(x2, y2);  
}  
   
function drawTree(x1, y1, angle, depth){  
  if (depth !== 0){  
    var x2 = x1 + (Math.cos(angle * deg_to_rad) * depth * 10.0);  
    var y2 = y1 + (Math.sin(angle * deg_to_rad) * depth * 10.0);  
    drawLine(x1, y1, x2, y2, depth);  
    drawTree(x2, y2, angle - 20, depth - 1);  
    drawTree(x2, y2, angle + 20, depth - 1);  
  }  
}  
   
context.beginPath();  
drawTree(300, 500, -90, depth);  
context.closePath();  
context.stroke();  
</script>

slice and dice

level:
- independent systems
- interdependent systems (app / db / auth) 
- components 
- packages
- class

proprties of good apis
- statelessness
- consistency
- clear parameter
- short parameter lists
- wrapper for complex operations


software architecture as api design


Everything is an API
-> a Class is the smallest API
-- Statelessness, Closed, The programmer is the enemy

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzk1OTI5NTQ2LDIxMTM1NjM2MzksLTE5OT
kzMTg3NzIsLTIwMjk1MzU4NTMsLTExMTc5NTg4ODcsNDA3ODI2
Nzk3LDIxMDk3Mjg0OTksMTE0NTY2MjkwM119
-->