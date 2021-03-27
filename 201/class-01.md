# What you need to know to build a website?
## First: How the web work?
When you visit a website
1- Your browser connects to a network of servers, called (DNS: domain name system servers).
2-	DNA return unique number to your computer that allows the browser to contact the web server that host the web.
3-	Then the web server sends the page to your browser. 
## Second: What is the components of a website?


![html,css,js]( https://www.10bestdesign.com/blog/content/images/2018/03/30.png)
![how html,css,js work together]( https://brutelogic.com.br/blog/wp-content/uploads/2020/03/html-js-css.jpg)

## HTML: Hypertext markup language
HTML Uses **Elements** to Describe the Structure of Pages. 

[HTML & CSS Design and Build Websites]( https://ltucasac.slack.com/files/U0137RDB5H6/F01RQKH7EBE/duckett_html.pdf?origin_team=TNGRRLUMA&origin_channel=C01RACEL21F)

### The elements contain of the components:
* Content within the tags
* Attributes of the tag: 
   provide additional information about the contents of an element. They appear on the opening tag of      the element and are made up of two parts: a name and a value, separated by an equals sign.
* A closing tag </ >
* An opening tag < >

![HTML element]( https://www.basictutorials.in/images/html-element.png)




The **TAGS** you add when you create a website known as a **MARKUP**


|            tags             |                                 description                                                            | 
|-----------------------------|--------------------------------------------------------------------------------------------------------|
| headings                    | html has six levels of heading &lt;h1: main heading…h6: the smallest&gt;                               |
| Paragraphs &lt;p&gt;        | contain a paragraphs inside its closing and opening tags                                               |
| **Bold**, *Italic*          | &lt;b&gt; , &lt;i&gt;                                                                                  | 
| &lt;s&gt;                   | indicate that is no longer there, ex:  when get cross over an old price in Ad.                         |
| &lt;sup&gt; , &lt;sub&gt;   | contain the element that is superscript or subscript                                                   |
| &lt;br&gt;                  | line break inside a paragraph                                                                          |
| &lt;hr&gt;                  | horizontal rule between sections                                                                       |
| &lt;!-- comment --&gt;      | what you wreat in the comment doesn't show or run in the code                                          |
| &lt;meta&gt;                | it is written inside the head, its description by the browser as keywords for the search               |




### main components in html code:
![htmlCode](https://zubairkhanqureshi.files.wordpress.com/2014/08/2.png?w=640)

* DOCTYPEs: declaration to tell a browser which version of HTML the page is using.
* Head : contains information about the page (rather than information that is shown within the main part of the browser window.
* Title : you find it in the head, shown in the top of the browser.
* Body : this element is shown inside the main browser window.

### ID & CLASS Attributes:
They both are used to give the elements uniquely identifying, which can be helpful when applying a style, the only difference that you can't apply the same id for more than one elementbut with class attribute you can.

### Block-element & Inline-element:
* Block elements are the elements the always start at new line.
* inline element are the element the start at the same line for the previous element.  

### what are semantic elements ? and why they are important?
When a browser communicates with the code, it looks for some specific information to help with the display. Hence, HTML5 introduced a consistent list of semantic elements to help search engines and developers.

HTML5 semantic tags define the purpose of the element. By using semantic markup, you help the browser understand the meaning of the content instead of just displaying it. By providing this extra level of clarity, HTML5 semantic elements also help search engines to read the page and find the required information faster.[bitdegree](https://www.bitdegree.org/learn/html5-semantic-tags)

|        smantic element           |          description                                                        |
|----------------------------------|-----------------------------------------------------------------------------|
| &lt;header&gt;                   | a header of your document, It is shown at the top of the page               |
| &lt;nav&gt;                      | represent the space for navigation links                                    |
| &lt;section&gt;                  | define a separate section within a webpage                                  |
| &lt;artical&gt;                  | define artical content in the webpag                                        |
| &lt;aside&gt;                    | defines the content which will be set to the side                           |
| &lt;footor&gt;                   | describes the footnote for your website                                     |
| &lt;main&gt;                     | main content of a page                                                      |
| &lt;img&gt;                      | to add image to the website                                                 |
| &lt;table&gt;                    | to creat table with rows and columns                                        |


![comparing between html5&html4](https://s3.amazonaws.com/viking_education/web_development/web_app_eng/html5_sectioning_high_level.jpg)

## JAVA SCRIPT: 
is an asynchronous, dynamicaly- typed, interpreted scripting language, designed to make web pages dynamic and interactive.

### What is a script and how we creat it ?
[javascript and jquery](https://slack-files.com/files-pri-safe/TNGRRLUMA-F01RRT6PRF0/javascript_and_jquery_interactive_jon_du.pdf?c=1616835435-d7b9f75479fd44fb)
* A script is a series of instructions that the computer can follow in order to achieve a goal. 
* Each time the script runs, it might only use a subset of all the instructions. 
* Computers approach tasks in a different way than humans, so your instructions must let the computer solve the task prggrammatically. 
* To approach writing a script, break down your goal into  a series of tasks and then work out each step needed to complete that task (a flowchart can help).

## how do you write a scripte for a web page?
the best way to start is to make a file (app.js) it is better to keep the JS & CSS files separated from the HTML index file, then we can link them to the html file.
![link CSS file inside html file](https://www.bitdegree.org/learn/storage/media/images/8c4493d3-110c-4a95-8b70-7626ce2d2f4e.jpg)
![link js inside html code](https://miro.medium.com/max/1654/1*09O6SLImZJDdwEaVae951g.png)

