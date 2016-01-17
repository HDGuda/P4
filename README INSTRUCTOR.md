What I did to improve the performance of the website:

PART 1:

In the index.html I introduced a media query to print.css. Now it is only loaded when needed for printing.

Changed the load mode for style.css to async to make it load asynchronously.

Resized and compressed pictures.

Changed the .htaccess to allow browser caching and data compression.



PART 2 - changes in main.js:

Improved the updatePositions function, which makes the pizzas fly in the background. Calling document.body.scrollTop every time in the loop caused a lot of Forced Synchronous Layout (FSL). I changed the formula a little bit to get rid of FSL (these flying pizzas in the background are stupid anyway).

Improved the changePizzaSizes function, too, to get rid of FSL. I simplyfied the way the new Pizza size is computed and changed.

After these improvements there was no jank, no FSL, and the page ran quickly and smoothly.
