## **MOD 01**

----

----

## A: Hello World <a name="helloWorld"></a>

If you: 
* Go to the [online p5.js editor](https://editor.p5js.org/) and
* Paste in this code:

        function setup() {
        createCanvas(400, 400);
        }

        function draw() {
        background(220);
        circle(150, 150, 300);
        }
* Click the Play button (upper left) 

You should see something like this:

![p5_01](https://user-images.githubusercontent.com/48248663/105062890-1a94bd80-5a49-11eb-8db6-3e0ea0b2f413.jpg)

The results on the right tell us at least these things: 

1. The Canvas itself is measured from its upper left corner

2. Circles are measured by by _diameter_, not the _radius_ 

3. Circles on the Canvas are located at their centers (_not_ their upper left corners)

----
> **CALCULATE:**  
* How do we know all this?

----

> **DOTHIS:**  
* Check the Auto-refresh box, upper left  
* Play with the numeric values of this code to discover what they mean to the result  
* Check out the [circle reference](https://p5js.org/reference/#/p5/circle) for p5.js  
* [Read about](https://cathyatseneca.gitbooks.io/introduction-to-p5-js/content/chapter1.html) p5.js

----

----

## What's my Function <a name="myFunction"></a>

A `function` is a set of instructions that must be followed _only and whenever_ the function is "called" -you can pass information to the function through its `parameters`

In the [Hello World](#helloWorld) section, above, we used two functions:
* `setup` creates a Canvas 400 pixels wide by 400 pixels tall

* `draw` draws on that Canvas: first a gray background, then a circle at location 150x, 150y with a diameter of 300 

----

> **RESEARCH:**  
* What do we mean by [x and y](https://learn365project.com/2015/08/01/why-do-computer-coordinates-start-from-the-upper-left-corner/)?

----

Ihe items inside the `{curly brackets}` of these functions are, in this case, also functions -the `(round brackets)` give them away

The round brackets are where we pass the `paramaters` to the functions

In your code from the [Hello World](#helloWorld) section replace the `draw` funtion with:

        function draw() {
        background(220);
        circle(150, 150, 300);
        rect(100, 150, 200, 100);
        }

The results on the right tell us at least these things:
1. Rectangles are drawn from their upper lefthand corners _-in contrast to circles_

2. Shapes appear on top of each other in the order in which they're drawn

----

> **DOTHIS:**
* Check out the [rect reference](https://p5js.org/reference/#/p5/rect) -with an eye to `tl tr br bl` parameters 
* Adjust your rectangle so that the top left and bottom right corners are _rounded_
* In the p5.js [reference](https://p5js.org/reference/), check out the _2D Primitives_ under the _Shape_ heading
* Stack up some more shapes
* Change their stacking order by changing the order in which they're drawn

----

----

## B: Color my World <a name="colorWorld"></a>

Make this your `draw` function:

       function draw() 
        {
        background(220);
           
          //red circle
          
        stroke(0, 0, 0);
        strokeWeight(1);
        fill(255, 0, 0);
        circle(150, 150, 300);
           
          //blu rect
          
        stroke(255, 204, 0);
        strokeWeight(12);
        fill(0 ,180, 255);
        rect(100, 150, 200, 100);
        }

We add color, determined by blending red, green and blue

> **RESEARCH:**  
* What do the double slash symbols `//` indicate, what are they for? 
* How will the browser treat all the  blank spaces I left in this code? 
* Get your head around [Stroke and Fill](https://stackoverflow.com/questions/4125152/difference-between-stroke-and-fill)


> **READING:**   
[Primary Colors of Painting and Light:](https://wtamu.edu/~cbaird/sq/2015/01/22/why-are-red-yellow-and-blue-the-primary-colors-in-painting-but-computer-screens-use-red-green-and-blue/#:~:text=This%20means%20that%20the%20primary,and%20blue%2Demitting%20light%20sources.)

> **INTERACTIVES:**  
[Color Picker](https://www.google.com/search?q=color+picker)  
[RGB Color Space](https://programmingdesignsystems.com/color/color-models-and-color-spaces/index.html)

> **MAKE:**  
This, or use it as inspiration for a thing you make  
It could be a face, a rainbow, a flower... 
![p5_02](https://happycoding.io/tutorials/p5js/images/calling-functions-2.png)

----
----

## C: What's my Function?

* **I. Values**  
You've been passing values to functions since you used a line like
`circle(200, 150 300)` and set the x and y _values_ for position and the _value_ of the circle's diameter

* **II. Operators**   
`+, -, *, /` are all operators, if you wanted to, you could have passed these values to the `circle()` function

`circle(150+50, 300/2, 30*10);`

* **III. Variables** 

GIVEN

Variables are _names_ that hold _values_

Variables are things we can _declare_ ourselves but some are given to us by p5.js, for instance:  
Width and Hight

                function setup() {
                createCanvas(500, 200);
                }

                function draw() {
                background(0, 200, 0);

                fill(255, 128, 0);
                ellipse(width/4, height/4,
                        width/2, height/2);
                ellipse(width*.75, height/4,
                        width/2, height/2);
                ellipse(width/4, height*.75,
                        width/2, height/2);
                ellipse(width*.75, height*.75,
                        width/2, height/2);

                fill(255, 0, 0);
                ellipse(width/2, height/2,
                        width/2, height/2);
                }

> **DOTHIS:**  
Change the values passed to the `createCanvas` function

> **CALCULATE:**
* What is [the difference between a `circle`](https://p5js.org/reference/#/p5/ellipse) [and an `ellipse`](https://p5js.org/reference/#/p5/ellipse) in p5.js?
* Describe in words what this `draw` function is doing

DECLARED  

Run this code in the [p5.js online editor](https://editor.p5js.org/) 

                function setup() {
                createCanvas(300, 300);
                }

                function draw() {
                background(32);
                //declare some variables
                let ellipseX = 150;
                let ellipseY = 200;
                let ellipseWidth = width/4;
                let ellipseHeight = height/2;
                //pass variable values to function
                ellipse(ellipseX, ellipseY, ellipseWidth, ellipseHeight);
                }

> **DOTHIS:**  
Change the values passed to the `createCanvas` function

>**CALCULATE:**  
If I make these values:  
`function setup() {`  
`createCanvas(100, 300);`  
`}`  
_What happens to my ellipse?_

* **IV. Random**  

You can generate a random number or chose randomly from an ordered list -[what we call an "array"](https://www.youtube.com/watch?v=ICb7iif9nFM)

* random([min], [max])

* random(choices)

This code will draw a flower in a random location at a random size (within limits, be careful not to draw everything off the canvas)

                function setup() {
                createCanvas(300, 300);
                frameRate(6);
                }

                function draw() {

                let flowerX = random(0, width);
                let flowerY = random(0, height);
                let petalSize = random(25, 150);
                let petalDistance = petalSize / 2;

                background(0, 200, 0);

                fill(255, 128, 0);

                // upper-left petal
                circle(flowerX - petalDistance, flowerY - petalDistance, petalSize);

                // upper-right petal
                circle(flowerX + petalDistance, flowerY - petalDistance, petalSize);

                // lower-left petal
                circle(flowerX - petalDistance, flowerY + petalDistance, petalSize);

                // lower-right petal
                circle(flowerX + petalDistance, flowerY + petalDistance, petalSize);

                // center petal
                fill(255, 0, 0);
                circle(flowerX, flowerY, petalSize);
                }

> **NOTE:**  
 p5.js runs your code inside the draw function 60 times a second, the `frameRate` value here given changes that to 6 times a second 

> **MAKE:**  
Using the random flower generator, above, as inspiration and peeking through the [random reference](https://p5js.org/reference/#/p5/random) see if you can make a sort of random word generator, or something similar to the flower generator that alternates between skulls and roses
Or, you know, anything
