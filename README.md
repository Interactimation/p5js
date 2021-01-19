# p5js
p5.js mini course  
by Mark Baldridge  
at Albright College

## MOD 01

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

The results on the right tell us at least two things: 

1. The Canvas itself is measured from its upper left corner

2. Objects on the Canvas are located at their centers (_not_ their upper left corners)

> **DOTHIS:**  
Check the Auto-refresh box, upper left  
Play with the parameters of this code to discover what they mean to the result  
