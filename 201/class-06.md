# Chapter 3: Objects


## What is Object?


Objects contain a group of functions and variables, the names changes the variables called **properties** and the functions called **method**.
The *name* for properties and methods called **key**.


## Notes: 


* an object cant have 2 kays with the same name


* the value of a property can be (string, Boolean, number, array or even anther object) but the value of a method cant be anything other than function.









## creating object by using Literal Notation 



![objects]( https://miro.medium.com/max/4096/1*GA7toY-Y3a3l0nlewOxIAw.png)



## Accessing properties and methods in objects by using (dot notation) or (square brackets) 



![Accessing]( https://dmitripavlutin.com/static/50a87420915de18f26da616865fe9825/05127/access-object-properties-2.png)  



# chapter 13: Documents objects model

## What is the Documents objects model 


specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.


## How to caching DOM queries?


Queries are the methods that find elements in DOM and if we need to use an element multiple times we should store queries result in a variable.
What we actually do we store element in a variable that we store the location of that element in the DOM tree.


![Dom]( https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSi6pz-Ow3WZW3JhnOQ5R75QeVzdx-0aYICLuvaxhIilM0TOqrimYdGKT4ivF0bwmS-EU0&usqp=CAU)


## How to select individual elements?

* getElementById()

* squerySelector()


## How to select an elements from Nodelist?


* The item() method. 
var elements = document.getElementsByClassName('hot') 
if (elements.length>= 1) { 
var firstltem = elements.item(O); 

* array syntax. 

ar elements = document.getElementsByClassName('hot') 
if (elements.length>= 1) { 
var firstltem = elements[0]; 


* Both require the index number of the element you want.

## you can loop through each node in a nodelist and apply the same statement for each one.

var hotlt ems = document .querySelectorAl l (' l i . hot') ;         //Store Nodel ist i n array 
if (hot ltems.length > O) { II If it contains i t ems 
for (var i=O; i&lt;  hotl tems.length; i++) {                        //Loop throug h each it em 
hotltems[i] .className = 'cool';                                     //Change val ue of class at tri bute 
 }
}

