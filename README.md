## Website Performance Optimization portfolio project

Both source and production code can be found in the folder.
Grunt was used to minify JS, CSS and HTML for production code.

####Part 1: Optimize PageSpeed Insights score for index.html

The work done:

1. CSS was inlined.
2. Images (profilepic and pizzeria) were optimized.
3. Google analytics script updated and async tag added
4. Added print attribute to the link to print CSS.

See the website [here](http://aviun.github.io/frontend-nanodegree-mobile-portfolio/dist)

And the Page Speed results [here](https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Faviun.github.io%2Ffrontend-nanodegree-mobile-portfolio%2Fdist)

####Part 2: Optimize Frames per Second in pizza.html

The work done:

Scrolling: 

1. The major bottleneck was found in updatePositions function. It was modified - calculation of position change was moved out of scope of the for loop.
2. Removed redundant variables.
3. querySelectorAll was replaced by getElementsByClassName and document.querySelector() was replaced with faster document.getElementById.
4. Mover class in CSS file was updated with transform property to push pizzas to another layer.
5. Dynamic counter of moving pizzas was added.

Resize pizza's time decreased:

1. changePizzaSizes function was modified, removed dx variable and determineDx function.
2. Repeated access to the DOM was moved out of the scope of the for loop.
3. Changed px values to % in changePizzaSizes

See the website [here](http://aviun.github.io/frontend-nanodegree-mobile-portfolio/dist/views/pizza.html)
