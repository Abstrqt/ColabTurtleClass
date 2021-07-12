<h1 align="center">ColabTurtleClass</h1>

<p align="center">
  <a href="https://github.com/Abstrqt/ColabTurtleClass/releases" target="_blank">
    <img alt="Release" src="https://img.shields.io/github/v/release/abstrqt/colabturtleclass?color=56bcd3">   
  </a>      
  <a href="https://pypi.org/project/ColabTurtleClass/" target="_blank">
    <img alt="Downloads" src="https://img.shields.io/pypi/dm/colabturtleclass?color=56bcd3">
  </a>      
  <a href="https://github.com/Abstrqt/ColabTurtleClass/blob/main/LICENSE" target="_blank">
    <img alt="License" src="https://img.shields.io/pypi/l/colabturtleclass?color=56bcd3">
  </a>      
</p>

Description
----
Class implementation of ColabTurtle by Tolga Atam. This library allows for multiple instances of turtles on one display. 


Installation for Google Colab:
----
Create an empty code cell and type:

    !pip3 install ColabTurtleClass

Run the code cell. Google Colab will install the library.


Usage
----
In any code cell, import the Window and Turtle classes:

    from ColabTurtleClass.Turtle import Turtle, Window

Create a Window object and turtle objects:

    window = Window()
    bob = Turtle(window)
    joe = Turtle(window)
    
Note that the constructor for the Window class takes one keyword argument `initial_window_size : tuple` and the constructor for the Turtle class takes one required argument `window : Window` and one keyword argument `initial_speed : int`. To have all turtles drawn on the same display, pass in the same Window object to each new Turtle object.

Example
----

The following code illustrates some usages of the library. For all functions available in this library, please check the API documentation below.

```
from ColabTurtleClass.Turtle import Turtle, Window

window = Window()
bob = Turtle(window)
joe = Turtle(window)
bob.color("blue")
joe.color("red")

for x in range(4):
  bob.forward(100)
  bob.right(90)

joe.penup()
joe.face(180)
joe.forward(150)
joe.pendown()
for x in range(3):
  joe.forward(100)
  joe.right(120)
```

This code ends up with the following drawing:

![Example of two turtles](https://github.com/Abstrqt/ColabTurtleClass/blob/main/example.PNG)


API
----
This module's API is mostly identical to the [ColabTurtle API](https://github.com/tolgaatam/ColabTurtle). Since the code was refactored into classes, some methods can only be called through their respective classes. The methods of the two classes are shown below:

##### Window Class

`bgcolor(colorstring)`
`window_width()`
`window_height()`

##### Turtle Class

`forward(units) | fd(units)`
`backward(units) | bk(units) | back(units)` 
`right(degrees) | rt(degrees)`
`face(degrees) | heading(degrees) | setheading(degrees)` 
`left(degrees) | lt(degrees)` 
`penup() | pu() | up()`
`pendown() | pd()`
`isdown()`
`speed(s)`
`setx(x)`
`sety(y)`
`home()`
`getx() | xcor()`
`gety() | ycor()` 
`position() | pos()`
`heading() | getheading()`
`goto(x,y) | setpos(x,y) | setposition(x,y)` 
`showturtle() | st()`
`hideturtle() | ht()`
`isvisible()` 
`color(colorstring) | pencolor(colorstring)`
`width(w) | pensize(w)`
`distance(x,y)`
`clear()` 
`write(obj, align=, font=)`
`shape(sh)`


Credits
----
Tolga Atam - ColabTurtle 
