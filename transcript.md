# Canvas
## Intro
Hi, everybody. My name is Kate and i want to tell you about “Canvas”. And let’s start from the first question: 
What is it?
HTML Canvas is an amazing drawing technology built into all modern browsers. 
With Canvas, you can draw shapes, manipulate photos, create games, 
and animate virtually anything - all with the right web standards. And you can also make mobile applications.
## How to use this html tag?
And now do you want to ask me: how to use this html tag? It's very easy.
To get started, you need to prepare the field on which we will draw. This field is done using the <canvas> tag, which should be specified with a width and height, content is controlled by contexts.
Then we need to get our drawing field, for example through getElementById. Let's write it to the variable canvas and do it like this: let ctx equally canvas.getContext ('2d'). 
The ctx variable is an object that contains the so-called execution context. All drawing will be done using the methods of this object.
As a result, you can see an area with a white rectangle.
## Rectangle
The most basic shape you can draw is a rectangle. There are three functions for drawing rectangles:
strokeRect - draws a rectangle
fillRect - draws a filled rectangle
clearRect - clears the area on the canvas the size of the given rectangle
An example illustrating how these functions work: 
in lines 3 and 4 we changed the size of the canvas,
in lines 5 and 6, we drew two uncolored rectangles that will symbolize a kind of frame of our "chessboard",
on line 7 we draw a filled rectangle whose dimensions would allow it to contain 64 squares with a side width of 32 pixels,
in lines 8 to 11, we have two loops that clear square areas on a black rectangle in such an order that the resulting image looks like a chessboard.
## Lines and arcs
What other shapes and shapes can you draw? Lines and arcs. Drawing shapes composed of lines is performed sequentially in several steps: beginPath() is used to "begin" a series of actions describing drawing a shape.
closePath() is an optional action and in essence it tries to complete drawing by drawing a line from the current position to the position from which you started drawing.
The final step is by calling the stroke or fill method. Actually, the first one outlines the shape with lines, and the second one fills the shape with a solid color.
So, there are methods like,
moveTo (x, y) - moves the "cursor" to position x, y and makes it current
lineTo (x, y) - leads the line from the current position to the specified one, and then makes the specified current one
arc (x, y, radius, startAngle, endAngle, anticlockwise) - draw an arc, where x and y are the center of the circle, then the start and end angle, the last parameter indicates the direction
This example shows the action of everything described above.
In line 7 the arc is filled with color, in line 15 the outline of our crown is outlined.
## Color
So that our image is not only two colors, but any color is provided, two properties. Change the color in the checkerboard example.
fillStyle - defines the fill color; strokeStyle - line color; 
## Image
The canvas api provides for interaction with images.
first line - Create a new image object, second - Path to the image to be applied to the canvas. To draw an image to the canvas used funcion drawImage - where x and y are the coordinates of the upper left corner of the image, and the first parameter is the image. The image is loaded immediately after the object is assigned an image source, otherwise it will simply not be drawn on the canvas. To avoid this situation, the following construction is used: between new object and path to image add An event that will be executed when the image is loaded.
Consider an elementary example: create the image, add image source and onload event with function, which draws an image.
So now we will try to scale the image, and for this there is another way to call the drawImage function:
The third call to drawImage with eight parameters looks something like this
## Example
And now I want to demonstrate what else HTML5 Canvas is possible for, here is a small selection of different and beautiful examples that you will definitely like
Rainbow rain. A really good example of animation running on Canvas, like rainbow rain is pouring from the sky. Looks very nice.
Game “Pong”. It’s a little pong game. Pong is the simplest table tennis simulator. A small square, replacing a ping-pong ball, moves along the screen along a linear path. If it hits the perimeter of the playing field or one of the drawn racquets, then its trajectory changes in accordance with the collision angle.
## The end!
Not all of Canvas has been demonstrated in this presentation. I encourage you to work with this tag in more detail, for example, create a game, add background and colors, animation, and add something else. Thanks for attention!
