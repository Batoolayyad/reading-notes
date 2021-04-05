# Chapter 6: “Tables” 

## How to build a table ?

* the element &lt;table&gt; 
To create table

* &lt;tr&gt; 
To determine where the table start

* &lt;td&gt; 
Its contain the table data


* &lt;th&gt;
it used like &lt;td&gt; but it Represent the heading for column or row.

* for long tables we use  &lt;thead&gt; ,&lt;tbody&gt; ,&lt;tfoot&gt;
 


![table](https://lh3.googleusercontent.com/proxy/f-_TWh-6tzxrncmOtGKHGMlo22b2EQP1MsYH-lg22fN2aWTJ4pys_VPhJMPs3EGK8UGT1WbsZYS19oUG72b6e2P4JJ6ywg-eTGPmXhc0IOF4UKAb1EiEdyobEfVUqijIzmLc-g)



You can make cells of a table span more than one row or column using the rowspan and colspan attributes.


# Chapter 3: “Functions, Methods, and Objects” 

 using **new** keyword with an object create blank object then you can add properities and method to it.
 when we use new we replece {} with **();** and at the end of each method or properties we add **;**.


**example**


var hotel : **new object();**
hotel rooms :25 **;**
hotel booked: 15 **;**

hotel .checkAvailability = function(){
return this.rooms - this.booked; 
} **;** 
 

 
 ## How to update value for propreties inside and object ?
 * by using the **Dot natation** 

example:
 **hotel.name =' stare';**
 
 
 * also you can use **[]** but not for methodes, example:
 **hotel.name =[  ];**

* you can delete by using **delete**, example:
**delete. hotel. name**

or rest the value, example:
**hotel.name='';**


## Arrays are objects
Arrays are a special type of object, but the different the kay for each value its index.


![arrays vs object](https://www.kirupa.com/javascript/images/array_shows.png)


  