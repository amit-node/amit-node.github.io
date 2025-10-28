---
title: Python Turtle
date: 2025-10-28
tags:
  - python
  - art
---
Turtle is a python library which used in making graphics (line art and drawings).  
Official documentation about turtle. [link](https://docs.python.org/3/library/turtle.html)  
w3school tutorial [link](https://www.w3schools.com/python/ref_module_turtle.asp). GeeksforGeeks is better [link](https://www.geeksforgeeks.org/python/turtle-programming-python)  

I am using turtle in thonny. Simple and easy. Thonny is a very light weight Python IDE for beginners, it's free, easy to use and very light and fast. [More about Thonny](https://thonny.org)  

```python
from turtle import *

speed(10)
forward(100)
right(90)
forward(100)
left(45)
back(50)

turtle.done()
```

square
```python
from turtle import *

for i in range(4):
    forward(100)
    right(90)

turtle.done()
```

think
```python
from turtle import *

for i in range(10):
    forward(100)
    right(60)

turtle.done()

```

think more
```python
from turtle import *

speed(10)

for i in range(100):
    forward(200)
    right(137.5)

turtle.done()
```

playing with Golden angle
```python
import turtle

t1 = turtle.Turtle()
t1.speed(10)
for i in range(500):
    t1.forward(200)
    t1.right(137.5)

t2 = turtle.Turtle()
t2.setposition(-200, 200)
t2.color("blue")
t2.speed(10)
for i in range(500):
    t2.forward(200)
    t2.right(137)

turtle.done()
```

just change angle
```python
from turtle import *
speed(10)

angle = 100
for i in range(10):
    forward(100)
    right(angle)
    forward(100)
    right(angle)
    forward(50)
    right(angle)
    forward(50)
    right(angle)
    forward(100)
    right(angle)
    forward(25)
    right(angle)
    forward(25)
    right(angle)

done()
```

```python
from turtle import *

speed(10)

circle(100)
circle(-50)

done()
```

```python
from turtle import *

speed(10)

circle(100, 180)
circle(-50)

done()
```

```python
from turtle import *

speed(10)

for i in range(10):
    circle(50, 120)
    left(105)

done()
```




















---

something really beautiful. Though I haven't understood it yet.
```python
import turtle

radius = 100
angular_speed = 2

window = turtle.Screen()
window.tracer(0)
window.bgcolor(50 / 255, 50 / 255, 50 / 255)

main_dot = turtle.Turtle()
main_dot.pensize(5)
main_dot.shape("circle")
main_dot.color(0, 160 / 255, 193 / 255)
main_dot.penup()
main_dot.setposition(0, -radius)
main_dot.pendown()

vertical_dot = turtle.Turtle()
vertical_dot.shape("circle")
vertical_dot.color(248 / 255, 237 / 255, 49 / 255)
vertical_dot.penup()
vertical_dot.setposition(
    main_dot.xcor() + 2 * radius,
    main_dot.ycor(),
)

vertical_plot = vertical_dot.clone()
vertical_plot.hideturtle()
start_x = int(vertical_plot.xcor())
# Get range of x-values from position of dot to edge of screen
x_range = range(start_x, window.window_width() // 2 + 1)
# Create a list to store the y-values to draw at each
# point in x_range.
vertical_values = [None for _ in x_range]
# You can populate the first item in this list
# with the dot's starting height
vertical_values[0] = vertical_plot.ycor()

horizontal_dot = turtle.Turtle()
horizontal_dot.shape("circle")
horizontal_dot.color(242 / 255, 114 / 255, 124 / 255)
horizontal_dot.penup()
horizontal_dot.setposition(
    main_dot.xcor(),
    main_dot.ycor() - radius,
)

while True:
    main_dot.circle(radius, angular_speed)

    vertical_dot.sety(main_dot.ycor())
    vertical_plot.clear()
    # Shift all values one place to the right
    vertical_values[2:] = vertical_values[
        : len(vertical_values) - 1
    ]
    # Record the current y-value as the first item
    # in the list
    vertical_values[0] = vertical_dot.ycor()
    # Plot all the y-values
    for x, y in zip(x_range, vertical_values):
        if y is not None:
            vertical_plot.setposition(x, y)
            vertical_plot.dot(5)

    horizontal_dot.setx(main_dot.xcor())

    window.update()

```
source : [python coding book](https://thepythoncodingbook.com/2022/05/08/do-you-really-know-what-sines-and-cosines-are-visualising-maths-using-python-and-turtle)