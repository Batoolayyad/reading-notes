# chapter 7: Forms



## What is the form and why it’s used?
Elements that use to collect information from visitors, forms also allow users to perform other functions online.

## How forms work ?


(HTML duckett book)

1-the user fills in a form and then presses a button to submit the information to the server.

2-The name of each form control is sent to the server along with the value the user enters or selects

3-The server processes the information using a programming language such as PHP, C#, VB.net, or Java. It may also store the information in a database.

4-The server creates a new page to send back to the browser based on the information received.





## How we build a form in HTML?



1-By using the element &lt;form&gt; with his attributes:



* action:
It has the url for the page on the server that will receive the information in the form when it is submitted.
* method:
Forms can sent by using two value of the method (get, post)
* Id





2- &lt;input&gt;  with the attributes:



* type : which defined the type of the input (password, text,..)
* name
* size, maxlength

example:

Username:  
Password:  

&lt;form action="http://www.example.com/login.php"&gt;  
&lt;p>Username:
 &lt;input type="text" name="username" size="15" 
 maxlength="30" /&gt;  
&lt;/p>
&lt;p>Password:
 &lt;input type="password" name="password" size="15" 
 maxlength="30" /&gt;  
&lt;/p&gt;  
&lt;/form&gt;  
 


# Chapter 14: Lists, Tables and Forms

## how to style order and unordered list ?


By using :
{ list-style-type: }
1-Ordered: 
* decimal 1 2 3 
* decimal-leading-zero 01 02 03
* lower-alpha a b c 
* upper-alpha A B C 
* lower-roman
* i. ii. iii. upper-roman I II III
2-Unordered :
* none 
* disc 
* circle
* square

 
 
 
 ## How to give tables a border?

By using the attribute
Td  {




border-bottom: 2px solid #111111; 





border-top: 1px solid #999;
}







# Chapter 6: Event

## what events mean?
It’s the way that the browser use to tell that something that something happened, for example to tell that the button get clicked or the page finish downloading.




## What banding mean ?
It means what event Im waiting to happened















## How to monitor the event that happened in all the children elements?
By using event delegation

