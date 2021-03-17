to build a web you will need :
html (hyper text markup language), to do the structure of the web.
css, to make the styling 
JS, to do the interactions and make the web a live.

HTML structures :

<head> 
  
  <title> </title>
  <meta> </meta>

</head> 

<body>
 
 <header> </header>
 <main> </main>
 <footer> </footer>

</body>

HTML uses elements has main components, which are:
-opening tag
-closing tag
-content within the tags
-attributes of the tag; Attributes provide additional information about the contents of an element , it is written on the opening tag and has contain of two parts name and value ,ex:
<p lang="en-us">

 
there are different versions of the HTML and before we start coding we should add the version that we work on on the top of our code for the browser

html5
<!DOCTYPE html>

html4
<!DOCTYPE html PUBLIC
"-//W3C//DTD HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd">

Transitional XHTML 1.0
<!DOCTYPE html PUBLIC
"-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/
 xhtml1-transitional.dtd">

Strict XHTML 1.0
<!DOCTYPE html PUBLIC
"-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/
 xhtml1-strict.dtd">

XML Declaration
<?xml version="1.0" ?>


** comments on Html <!--comment-->

some common attributes:
-ID attribute; to identify that element from other elements on the page <p id="nomber1"> part of a paragraph </p>
-class attribute; to identify several elements as being different from the other elements on the page <p class="important">

* block elements & inline elements:
block elements start on a new line in the browser window while inline elements appear to continue on the same line as their neighboring elements.

* HTML5 introduces a new set of elements that allow you to divide up the parts of a page, Older browsers that do not know the new HTML5 elements will automatically treat them as inline elements, so we add a css line:
header, section, footer, aside, nav, article, figure
{
display: block;}

chapter 18:
when you build a website you need to understand the target audience, build a Wireframes which  is a simple sketch of the key information that needs to go on each page of a site and the importance of the styling.