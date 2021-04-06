
# chapter 15: layout

## CSS classified element into a three types, look at the example in the figure below :



* Block: start from a new line 

* Inline block: the same line but it surrounded with a box 

* Inline element: same line and not surrounding with a box



![block, inline block, inline element](https://i1.wp.com/www.tutorialbrain.com/wp-content/uploads/2019/06/CSS-Display.png?fit=474%2C379&ssl=1)
 


## what is the parent or the Container element?
 the outer box that has anther block level element inside it.


## How we control the position of elements?


* normal flow: the block level elements will sit under each other in new lines.


* relative position :you can change the element position anywhere but within the container box (stay inside the parents).

p.example { position: relative; 
top: 10px;
 left: 100px;}


* Absolute position: you can change the element position anywhere in the screen.

 h1 { position: absolute;
 top: 0px;
 left: 500px; 
width: 250px;}



## How various devices have different screen sizes and resolution, and how this affects the design process?


 Resolution refers to the number of dots a screen shows per inch. some devices allow the user to adjust the resolution of the display or the numbe of pixels. note that the higher Resolution  the smaller the text appears.
 Because screen sizes and display resolutions vary so much, web designers often try to create pages of around 960-1000 pixels wide 
(since most users will be able to see designs this wide on their screens).

## what are the Fixed layout and the Liquid layout?

* **fixed layout**: the size stay fixed and doesnt change when user change the size of thier browser window.


* **Liquid layout**: the desgin change as the user change the size of the browser window.


