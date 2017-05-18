## Website Performance Optimization portfolio project
The goal was to optimize a given website so that each page reaches a page speed of at least 90 measured with Page Speed Insights.

To get started, check out the repository and inspect the code.

### Getting Started instructions
1. Check out the repository
2. Run a local server through command line

 $> cd /path/to/root-project-folder/dist
 $> python -m SimpleHTTPServer 8080

3. Open a browser and visit localhost:8080
4. Download and install ngrok in the root of the project to make the local server accessible remotely.

   $> cd /path/to/root-project-folder/dist
   $> ngrok 8080
   
5. Copy the forwarded public URL ngrok provides and run it through PageSpeed Insights.
6. For testing the results for part 2  optimizations run the pizza.html in a browser.And check the timeline tab to record the
   events.Check the console to see the time taken to resize the pizza as well as frames per second.


### Part 1: Optimize PageSpeed Insights score for index.html

#### Optimizations made :

index.html

  * Make google-analytics script async
  * Add a media query for print.css
  * Inline css/style.css
  * Minify HTML
  * Minify CSS
  * Compress images
  * Use Web Font Loader to load the Google web fonts asynchronously
  * Placed scripts before tag closing </body> tag.

#### Result: The Google PageSpeed Insight Score for the mobile version of index.html changed to 91/100 and desktop version to 93/100.

#### Part 2: Optimize Frames per Second in pizza.html

  * Replaced querySelectorAll with getElementsByClassName for better performance
  * Replaced querySelector with getElementsById in function determineDx.
  * Moved the newwidth calculation inside the changePizzaSizes function out of the loop
  * Created a new variable to hold all of the .randomPizzaContainer elements in the document and looped through the elements to apply       the new width value.
  * Moved the calculation which utilizes the scrollTop method outside of the loop.
  * Declare var elem outside the loop to prevent it being created each iteration
  * Reduced the amount of animated pizzas from 200 to 32





