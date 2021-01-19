# p5.js
mini course  
by Mark Baldridge  
at Albright College

## MOD 01

----

----

## Hello World <a name="helloWorld"></a>

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

## Color my World <a name="colorWorld"></a>

Make this your `draw` function:

       function draw() {
        background(220);
        fill(255, 0, 0);
        circle(150, 150, 300);
        fill(0 , 0, 255);
        rect(100, 150, 200, 100);
        }
