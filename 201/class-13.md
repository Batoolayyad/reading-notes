
# THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS

persistent local storage is one of the areas where native client applications have held an advantage over web applications.
For native applications, the operating system provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state.


### cookies:
can be use for persistent local storage of small amounts of data. But they have three disadvantages:

- Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
- Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)
- Cookies are limited to 4 KB of data — enough to slow down your application, but not enough to be terribly useful


### A BRIEF HISTORY OF LOCAL STORAGE HACKS BEFORE HTML5:

Microsoft invented a great many things and included them in their browser one of them was called DHTML Behaviors, and one of these behaviors was called userData.
**userData** allows web pages to store up to 64 KB of data per domain, in a hierarchical XML-based structure.


In 2002, Adobe introduced a feature in **Flash 6** that gained the unfortunate and misleading name of “Flash cookies.”Flash gives each domain 100 KB of storage “for free.” Beyond that, it prompts the user for each order of magnitude increase in data storage (1 Mb, 10 Mb, and so on).


In 2007, Google launched **Gears**, an open source browser plugin aimed at providing additional capabilities in browsers.Gears can store unlimited amounts of data per domain in SQL database tables.


In the meantime, Brad Neuberg and others continued to hack away on dojox.storage to provide a unified interface to all these different plugins and APIs. By 2009, dojox.storage could auto-detect (and provide a unified interface on top of) Adobe Flash, Gears, Adobe AIR, and an early prototype of HTML5 storage that was only implemented in older versions of Firefox.


### INTRODUCING HTML5 STORAGE:
 it’s a way for web pages to store named key/value pairs locally, within the client web browser. 

 #### what is the differences and similarites between html5 and the cookies?
Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to the remote web server (unless you go out of your way to send it manually).

[diveinto](http://diveinto.html5doctor.com/storage.html)

