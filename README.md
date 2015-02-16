*Improving The Website's Performance

**Table Of Contents

1. Initial Assessment
2. Optimizations Performed On Index Page
3. Optimizations Performed On Mobile Web Development Page
4. Optimizations Performed On Pizza Page
5. Resources Utilized
6. Synopsis

** Initial Assessment

***Home Page
When looking at the Home Page, I saw that the Page Speed Score was 29

***2048 Page
This page had a Page Speed of 92

***Website Performance Optimization Page
This page had a Page Speed Score of 93

***Mobile Web Dev Course 
This page had a Page Speed Score of 87, which will need to be addressed

***Cam's Pizzeria 
This page had a Page Speed Score of 29, and the frame rate on scrolling was no where near 60 fps. Also, the Pizza resizer was above the requirement of 5ms.

2. Optimizations Performed On Index Page
 -Resized pizzeria image to be thumbnail size (100px x 75px)
 -Minified CSS files
 -Added async attribute to analytics and secondary .js files
 - Increased Page Speed Score to 93 (can be seen at page-rank/home-page-rank.jpg)

3. Optimizations Peformed On Mobile Web Development Page
 -Resized main image to be 602px x 306px. Increased Page Speed Score from 87 to 93 (can be seen at page-rank/mobile-page-rank.jpg).

4. Optimizations Performed On Pizza Page
 -Minified and compressed CSS Files
 -Minified and compressed JS Files
 -Minified and compressed HTML
 -Refactored changePizzaSizes() function to reduce the time it takes to change the pizza sizes. This was accomplished by pulling out the variables being rewritten within the for loop, to be
  just outside of the for loop scope. This was done because they only needed to be instantiated once, which greatly reduced resources. The variables within the for loop itself were declared
  outside, as this saved ~4ms. While not a great optimization, it does help to speed up the application. This micro optimization technique is discussed in JavaScript Patterns, by Stoyan Stefanov pages 15-16. This function now executes at ~1ms (as seen in page-rank/pizza-resize-time.jpg).
 -Refactored updatePositions() function to increase the FPS to 60. This was accomplished by caching the document.body.scrollTop method, instead of recalculating it on every scroll event.
  This technique was observed from the supplemented material, https://www.igvita.com/slides/2012/devtools-tips-and-tricks/jank-demo.html, where I reverse engineered the code to understand
  how to minimized the scroll call. An image has been included to show the frame rate was under 60 fps for me (can be seen at page-rank/pizza-timeline.jpg)
 -Resized the main image at the top to be at the size the page displays the content
 -Increased the Page Speed Score to be 92, as seen in page-rank/page-speed-pizza.jpg.

**Resources Utilized
Aside from the resources mentioned within the Pizzeria section, there were a couple additional resources utilized for the page optimizations:
	1) JavaScript was compressed utilizing jscompress.com
	2) CSS was compressed utilizing cssminified.css
	3) HTML was compressed utilizing kangax.github.io/html-minifier (pizza.html page only)

In this project, I utilized external resources for optimizing the web pages. For my typical product sites, I have a lot of this automated as I utilized various plugins in Sublime Text 2. For instance, I typically develop with Sass which allows me to compile various CSS files together into a singular file, and minifies it on save. This saves me time, as I don't have to manually initiate other tools for accomplishing this.

**Synopsis
I enjoyed this project quite a bit, as I love optimizing a web page to improve a user's experience. It was both a joy and a challenge to dive deeper within the Chrome dev tools to optimize the page; one that I look forward to utilizing more in my other web projects.