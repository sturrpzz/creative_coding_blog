---
title: Difficulties and Solutions
publish_date: 2023-03-31
abstract: Problems I faced with my codes and how I resolved them.
disable_html_sanitization: true
---

# Lack of knowledge on JavaScript

<iframe width="500" height="542" src="https://editor.p5js.org/ndeji69/full/EA17R4HHa"></iframe>

I was quite ambitious with my first sketch: I wanted to create swirling curves that interacts with the cursor. This sketch was my first inspiration. However, I wanted to make something that I understood, not copying others' codes without understanding anything.

# Struggle to make ellipse stroke change color

At first, I used `fill(‘color’)`, however, in this case, it didn’t work because `fill(‘color’)` is applied to the inside of the ellipse, not the strokes. After that, I tried using `stroke(random(255),random(255),random(255))`, but it would change the color of the strokes every frame, which was not what I wanted.

## Solution:

The color data should be applied to the strokes in a way that it is preserved and can be retrieved in the next frame, which means it cannot be in the draw function because the draw function would call the variable in every frame. It also cannot be in setup function either, because the variable would only be called once.

What I needed to do was to create a variable declared in the global scope and a custom function for the color randomization, with the variable given as an argument to the ellipse strokes.

```Javascript
let col = `red`

function rand_col () {
  const colors = random ('r','g','b')
    r = random(255)
    g = random(255)
    b = random(255)
  return color (r, g, b)
}

```

# Unable to load font pt.1: 

Because I put '' inside textFont() :D

# Unable to load font pt.2:

I used preload function to load some custom fonts at the beginning of the code, thinking it would have a similar effect as being in a global scope. Then, I tried applying these fonts to my class.

```Javascript

class Text {
  constructor (words, x, y, customfont, color, size) {
    this.content = words
    this.x_axis = x
    this.y_axis = y
    this.font_style = customfont
    this.font_color = color
    this.font_size = size
  }
  create () { 
    fill (this.font_color)
    textSize (this.font_size)
    textFont (this.font_style)
    text (this.content, this.x_axis, this.y_axis)
  }
}

const RMIT = new Text ('RMIT', 300, 110, lemonmilk, 'red', 110)
const CC = new Text ('Creative Coding', 280, 180, louisgeogrecafe, 'red', 40)
const Specialisation = new Text ('Specialisation', 320, 225, louisgeogrecafe, 'red', 40)
```

However, the fonts would not load. 

## Solution
Since everything in the global scope always happen first, when I declared my class, the preload function has not happened. I decided to use `textFont()` in draw function, and removed `customfont` from my class.

```Javascript

function draw {
    //Creative Coding Specialisation
    textFont (louisgeogrecafe)
    CC.create ()
    Specialisation.create ()  

    //RMIT
    textFont (lemonmilk)
    RMIT.create () 
}

```


