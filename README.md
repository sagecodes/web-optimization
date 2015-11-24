## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository, inspect the code,

####Part 1: Optimize PageSpeed Insights score for index.html
**What was done to exceed requirments of task 1:**

- Utilized gulp.js to:
    - Minify and concatenate CSS files
    - Minify Javascript files
    - minify HTML files
    - OPtimize images
- Manually optimized pizzeria.jpg to change the dimensions
- Move link to load css files to the bottom of the html body to offset render blocking

Page speeds are now at 93 - 95. Further performance enhancements could be made on the server side. Future improvements include: More Streamlined gulp tasks(or run multiple tasks), inline-css and JS when appropriate, use script to load in css with async property.



####Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js.


**What was done to meet requirements for task 2:**

- Refactor changePizzaSizes. no more query selecting for each element or conversions back to pixel and percentages(Similar to solution in lesson 5). *Resize time is now Aprox 1.7ms.*
- re-factor for loop and scroll events/animations. *page now scrolls smoothly. scroll animations are often under 1ms. occasionally longer animations show in dev-tools, but have not been notable in user experience.*
- minify js file



### How to run the project

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! * Note that the first time you run it you may get a slow server response time. If that's the case please re-analyze.


### Other sources used:

- Treehouse Gulp basics
- [Gulp for beginners - css tricks](https://css-tricks.com/gulp-for-beginners/)
- [page speed insights - google](https://developers.google.com/speed/pagespeed/insights/)
- [speed animations - html5Rocks](http://www.html5rocks.com/en/tutorials/speed/animations/)