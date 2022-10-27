# bouncing-balls
A MIT xPro coding boot camp project

## Original scope
The original scope asked us to create a bouncing ball that changed direction on hitting an arbitrarily decided limit.  The solution provided used a variable to track ball direction, but since I was already tracking velocity, I just made the velocity negative instead. Then I went a bit overboard on making it fancy.

## My improvements
The original design of the program had a number of premade balls created in document elements.  I decided to abstract the ball creation/movement so I could easily update how many balls were created. The HTML DOM is impressively powerful for this. The createElement method allowed me to generate the div elements for each ball programmatically instead of manually. An object for each ball had a link to the element, a random size, velocity, z-index, starting position and colour.  

Randomizing the colour was a bit of a challenge. The class solution did it using an array of colour names. Stack Overflow provided a bunch of complex ways to do it more broadly, but https://lnkd.in/ghmUR9Vi taught me that you can cast from decimal to hex using toString in javascript - total game changer. I set it to change every time it hit the top or bottom of the bounding box.

## Additional changes
2022 Oct 16 A classmate had her bouncing object in front of a video.  I thought it was cute so I added it.
2022 Oct 16 Added a countdown timer to stop each ball at some future time.  
2022 Oct 18 Improved the iteration process.


## Future plans
* The counter for the countdown runs in the background even after all balls are stationary - it'd be nicer if this could stop and the script could stop calling setInterval.
* I've played around a bit adding gravity and drag, but that seems to be overly complex for this scope of project.
* I'm considering just grabbing the current state of each ball from the document on each iteration, instead of storing it in an array, and may wind up taking a stab at that some time down the road.
* I may also add inputs at the beginning to indicate the number of balls, the time frame, etc.
* Instead of arbitrarily setting limits, I may have the script grab it from the window properties.
