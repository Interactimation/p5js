

## **MOD 01**

**SUBJECT INDEX** <a name="index01"></a>

[Hello (Canvas) World](#helloWorld)    
[What's my Function](#myFunction)  
[Color my World](#colorWorld)  
[Variable Weather](#variableWeather)  
[Totally Rnadom](#totalRandom)   

----

----

## Hello (Canvas) World <a name="helloWorld"></a>

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

[Back to Top](#index)

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

[Back to Top](#index01)

----

## Color my World <a name="colorWorld"></a>

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

[Back to Top](#index01)

----

## Variable Weather <a name="variableWeather"></a>

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

----

[Back to Top](#index01)

----

## Totally Rnadom <a name="totalRandom"></a>

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

----

[Back to Top](#index01)

----

----



## **MOD 02**

**SUBJECT INDEX** <a name="index02"></a>

[Fully Functional](#fullFunction)  
[What's Bugging You?](#whatBug)
[Some Consolation](#consolation)
[Smooth Operator](#booleans)
[Or Else!](#orElse) 
[Inputtin](#input)

----

----

## Fully Functional <a name="fullFunction"></a>

You can create and "call" your own functions  
In the [online editor](https://editor.p5js.org/), after the `setup` function, paste this code:

        function draw() {
        background(32);
        drawRedCircle(100, 200, 50);
        }

        function drawRedCircle(circleX, circleY, circleDiameter) {
        fill(255, 0, 0);
        circle(circleX, circleY, circleDiameter);
        }

The function `drawRedCircle` could be any function you create  
You can "call the function" and pass parameters in the `draw` function, as here

----

> **DOTHIS:**  
Write -and call, in the `draw` function- your own function that draws a whole flower or other complex image using 
* basic shapes [(See 2D Primitives under Shape on this page)](https://p5js.org/reference/#/p5) 
* Some random-valued variables and
* A simple `frameRate()` animation, changing some parameter over time

BONUS POINT: If I say _"make all the flower centers (or eye colors or whatever elements appear on your canvas) blue instead of yellow"_ and you can do that by changing the value of a single variable 

----

[Back to Top](#index02)

----

## What's Bugging You? <a name="whatBug"></a>

Your code will develop "bugs" flaws that prevent it from performing the way it "should"

**FIRST:** INTERROGATE YOUR RESULT  
* Is it any good? I urge you to  
ARCHIVE THE GLITCH STATES  
of your code -a quick paste-into-plaintext or save-as glitchfile.js (I use [Visual Studio Code]https://code.visualstudio.com/() which I also recommend) 
* Can you see from your result where you went wrong?

I can only say that these will be the rare occasions  
Chances are there's no result, or the change you think you made does not appear  

**SECOND:** COUNT THE CURLY BRACKETS
This is shorthand for  
CHECK YOUR SYNTAX
Run this code in the [online editor](https://editor.p5js.org/) 


        function setup() {
        createCanvas(400, 400);
        }

        function draw {
        background(220);
        }

You might notice the preview shows no result but the actual "lines of code" are highlighted on the left and, below, the "console" shows an error

Neither of these tells you exactly the problem but compare the `draw` function with the `setup` function and see if you can spot the difference

**THIRD:** CHECK THE REFERENCE
If it's tough for you (like me) to rememBEr the syntax of every little thing, keep a bookmark on [the p5.js reference](https://p5js.org/reference/#/p5) 

**FOURTH:** THINK THROUGH YOUR CODE  
Explain what your code is SUPPOSED to be doing, to a rubber duck  
(Explain it out loud)

**FIFTH:** ASK FOR HELP  
If you haven't already done all the previous steps, you're not ready for this step

----

[Back to Top](#index02)

----

## Some Consolation <a name="consolation"></a>

This business with the console is going to come in handy: 

You can write anything you like to the console, and use this to test some things -has a variable changed its value? Has a new X position been randomly chosen?

Here I write the term "Frame Count" amd apply the frame count number to the console whenever the `draw` function runs

        function draw (){
        background(220);
        console.log("Frame Count: " + frameCount);
        }

Try it yourself and check the console  
See if it tells you anything about what's going on behind the scenes on a p5.js canvas!

----

[Back to Top](#index)

----

## Smooth Operator <a name="booleans"></a>

        If I set a couple variables like this
                
        function setup() {
        createCanvas(400, 400);
        }
        let score = 95;
        let isGradeA = score >= 90;
        console.log(isGradeA);

I've straightforwardly assigned the value of 95 to the variable `score`
I've created the `isGradeA` variable and assigned it a test: 
* Is `score` greater than or equal to 90? 
* And since it, in this cae, certain ly is, we've set the variable's [boolean value](https://p5js.org/examples/data-true-and-false.html) to `true` (which also has the value: 1) -the only other possible value is `false` (which also has the value: 0)  

----

[Back to Top](#index02)

----

## Or Else! <a name="orElse"></a>

This code demonstrates several things:

        function setup() {
        createCanvas(200, 100);
        background(200);
        }

        function draw() {
        let score = 95;
        let isGradeA = score >= 90;

        if (isGradeA) {
            background(0, 255, 0);
            fill(0);
            textSize(18);
            text('Congratulations!', 30, 55);
            }
        }

* That the `true` boolean value of a variable can be used to trigger a function
* How to draw `text`
* How to write an `if` statement

Set `value = 85` and see what happens  
Maybe you want a specific message for that condition  
What you want now is an IF, ELSE
Replace the `draw` function, above, with this: 

        function draw() {
        let score = 85;
        let isGradeA = score >= 90;

        if (isGradeA) {
            background(0, 255, 0);
            fill(0);
            textSize(18);
            text('Congratulations!', 30, 55);
            }
          else {
          background(255, 0, 0);
            fill(0);
            textSize(18);
            text('Study Harder!', 30, 55);
          }
        }

Now, if the `score` value is equal to or highter than 90 we'll get one result and anther if its lower

> **RESEARCH:**  
If you try to use a non-boolean value in an if statement, then the code uses the “truthiness” of that value to convert it to a boolean  
Values like 0, '' (empty string), and undefined are “falsy” and convert to false, and values like '42' and 'hello world' are “truthy” and convert to true

----

[Back to Top](#index02)

----

## Inputin <a name="input"></a>

So far, we've input all the values (even random ones) ourselves  
Interactivity relies on inputs from the "user"  

Ine way is to record the position of the cursor and when and where it clicks

This code creates a drawing app

        function setup() {
        createCanvas(600, 600);
        background(32);
        }

        function draw() {
        if (mouseIsPressed) {
            circle(mouseX, mouseY, 25);
        }
        }

> **CALCULATE:** 
Why does this circle draw over itself, not draw itself new every frame?
HINT: Check where the background ins being drawn -if we draw the background in the `draw` function, how will the result differ?

> **DOTHIS:**
* Make the `stroke` of the circle either the same color as the circle, [or give it no stroke](https://p5js.org/reference/#/p5/noStroke) 


> **DID WE MENTION?:**  
You can sign up with the p5.js editor (or sign in with GitHub) which will allow you to save and share your code  
Here's the above, editable:
https://editor.p5js.org/markbaldridge/sketches/ygH8fiIA0O

> **CHEAT SHEET**  
[This" Cheat Sheet shows some of the user inputs you can use](https://editor.p5js.org/markbaldridge/sketches/ygH8fiIA0O)

(You'll probably have to click into the preview field to get responses from some things, like keyCode, etc)

----

[Back to Top](#index02)

----

----







