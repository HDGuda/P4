Usage: Load index.html and click on Cam's Pizzeria.


What I did to improve the performance of the website:

PART 1:

In the index.html I introduced a media query to print.css. Now it is only loaded when needed for printing.

Inlined style.css.

Resized and compressed pictures.

Changed the .htaccess to allow browser caching and data compression.


PART 2 - changes in main.js:

I replaced querySelectorAll() with getElementsByClassName() because it is faster (credits: the reviewer). 

Improved the updatePositions function, which makes the pizzas fly in the background. Calling document.body.scrollTop every time in the loop caused a lot of Forced Synchronous Layout (FSL). I changed the formula to get rid of FSL (credits: the reviewer).

Improved the changePizzaSizes function, too, to get rid of FSL. I simplyfied the way the new Pizza size is computed and changed.

After these improvements there was no jank, no FSL, and the page ran quickly and smoothly.

Recalculated the numbers of flying pizzas (credits: the reviewer).

