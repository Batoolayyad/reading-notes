# Lists
Type of lists in HTML (look at the two figures below ):
* Unordered HTML List
  items will be marked with bullets (small black circles)
* Ordered HTML List
Items will be marked with numbers 
* HTML Definition  Lists
It contains terms with the definition.

| Tag	                | Description                                  |
|-----------------------|----------------------------------------------|
| &lt;ul&gt;	        | Defines an unordered list                    |
| &lt;ol&gt;	        |  Defines an ordered list                     |
| &lt;li&gt;	        |  Defines a list item                         |
| &lt;dl&gt;	        |  Defines a description list                  |
| &lt;dt&gt;	        |  Defines a term in a description list        |
| &lt;dd&gt;	        |  Describes the term in a description list    |




[w3schools]( https://www.w3schools.com/html/html_lists.asp)

![ordered and unordered lists]( https://cdn.clickworker.com/wp-content/uploads/2015/03/Bildschirmfoto-2015-03-23-um-15.51.48.png)
![ Definition Lists]( https://images.slideplayer.com/8/2430756/slides/slide_16.jpg) 

Nested list: sub list you can add insid the &lt;li&gt; tag
# Boxes

As shown in the figure below, the items in the html code are treated as blocks each block could have a specific design and you can make a lot of changes like the ones that we will cover on this chapter by using **CSS**:
* Controlling size of boxes.
* Box model for borders, margin and padding
* Displaying and hiding boxes.



![boxes in HTML1]( https://apprize.best/html5/way/way.files/image035.jpg)



**Controlling size of boxes**
This can be done by using the width and height 
'''html
Div {
Height'400px';
Width: '200px'; }
'''


**Border, Margin & Padding**
look at the figure below, we use the to add space between different items, to make the items easier to recognize and make the general design looks better.



![boxes in HTML2]( https://i.stack.imgur.com/cP5Oo.jpg)


* to chang border width, style, color we use:

 p{
    
    border-top-width, style or color
    
    border-right-width, style or color
    
    border-bottom-width, style or color
    
    border-left-width,style or color
 }

we also can make an image border by css3.


* to change padding :

nav {
    
    padding-top
    
    padding-right
    
    padding-bottom
    
    padding-left
}

ex: nav {padding: 10px 5px 3px 1px;}

* to change the margin:

h1{
    
    margin-top
    
    margin-right
    
    margin-bottom
    
    margin-left
}

ex: h1{margin: 1px 2px 3px 4px;}, (where the values are in clockwise order: top, right, bottom, left).

# basic java script :
## Arrays : type of variable the store list of values.

**How we right array in JS?**

var fruit 


fruit ('banana ' , 'apple', 'orange'); 

# Decisions and loops:
 
 ## If statement:

What if statement do is checking a condition if its true the code inside the if statement run, if its false the code in side **else** run. 
We can add more then one condition by using **else if**, look at the example below:


![if statement](https://www.learnbyexample.org/wp-content/uploads/r/r-if-else-if-else-statement-syntax.png)


## Switch:

it works the same as IF statement but for switch we can add more then one variable for the same condition. look the example below:

![switch](https://2.bp.blogspot.com/-XUiJMULtK1A/Vr3yoIN9b8I/AAAAAAAAAD8/WikSgHfKdYI/s1600/Syntax-of-Switch-Case-Stetement-in-C-Programming.jpg)


# Loops

 types of loop: for, while, do while. Each repeats a set of statements. look the example below. 
 the different between them 
 - while doesnt have a specific numbers of repeats, it doesn't go out of the loop until the condition become true
 - for has specific numbers of repeats 


 ![loops](https://slidetodoc.com/presentation_image_h/ea31c3f96b49add5f3671309afeadd81/image-11.jpg)
  

# Pass Functions Between Components


### In the video, what is the first step that the developer does to pass functions between components?
creat the function wherever the state that we are going to change
### In your own words, what does the increment function do?
receiving the arrays item, loop through the array and find the matching one to update
### How can you pass a method from a parent component into a child component?
by passing it as passing it as a props
### How does the child component invoke a method that was passed to it from a parent component?
by using special attribute that attach to the component ( Refs. React)