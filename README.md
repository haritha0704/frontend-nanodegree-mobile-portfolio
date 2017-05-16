## Website Performance Optimization portfolio project
The goal was to optimize a given website so that each page reaches a page speed of at least 90 measured with Page Speed Insights.

To get started, check out the repository and inspect the code.

### Getting started

#### Part 1: Optimize PageSpeed Insights score for index.html

##Optimizations:

index.html

  * Make google-analytics script async
  * Add a media query for print.css
  * Inline css/style.css
  * Minify HTML
  * Minify CSS
  * Compress images
  * Use Web Font Loader to load the Google web fonts asynchronously
  * Placed scripts before tag closing </body> tag.

Result: The Google PageSpeed Insight Score for the mobile version of index.html changed to 91/100 and desktop version to 93/100.


Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

#### Part 2: Optimize Frames per Second in pizza.html

  * Replaced querySelectorAll with getElementsByClassName for better performance
  * Replaced querySelector with getElementsById in function determineDx.
  * Moved the newwidth calculation inside the changePizzaSizes function out of the loop
  * Created a new variable to hold all of the .randomPizzaContainer elements in the document and looped through the elements to apply       the new width value.
  * Moved the calculation which utilizes the scrollTop method outside of the loop.
  * Declare var elem outside the loop to prevent it being created each iteration
  * Reduced the amount of animated pizzas from 200 to 32





