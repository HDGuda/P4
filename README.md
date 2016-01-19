Usage: Load index.html and click on Cam's Pizzeria.


What I did to improve the performance of the website:

PART 1:

In the index.html I introduced a media query to print.css. Now it is only loaded when needed for printing.

Inlined style.css.

Resized and compressed pictures.

Changed the .htaccess to allow browser caching and data compression.


PART 2 - changes in main.js:

I replaced querySelectorAll() with getElementsByClassName() because it is faster. 

Improved the updatePositions function, which makes the pizzas fly in the background. Calling document.body.scrollTop every time in the loop caused a lot of Forced Synchronous Layout (FSL). I changed the formula to get rid of FSL (credits: the reviewer).

Improved the changePizzaSizes function, too, to get rid of FSL. I simplyfied the way the new Pizza size is computed and changed.

Reduced the numbers of flying pizzas.

Replaced document.querySelector by document.getElementById in lines 410, 413, 416, 472.

Changed the use of variables in the for-loop in line 455.

Lines 540 and 550: Introduced new local variable and used getElementbyId instead of querySelector.

