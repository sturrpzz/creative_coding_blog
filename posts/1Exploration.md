---
title: Exploration
publish_date: 2023-03-31
disable_html_sanitization: true
---
# Sketch
I created a sketch of what I wanted to include in my design. 

When I thought about Javascript, the 3 keywords that came to my mind are **flexibility**, **layers**, and **functionality**. Unlike HTML and CSS, Javascript is like drawing on a canvas, which offers so many possibilities and so much flexibility. Layer was the second thing that came to my mind simply because the order of codes can change the layout of the canvas; and lastly, functionality is important for every coding language. 

When speaking of design elements, curves and ellipses are the most flexible there are. I want to incorporate layers into those elements to portray design principles of repetition, balance and movement. For the “RMIT Creative Coding Specialisation” text, I would like to apply a bold, thick sans-serif font to express a sense of modernity and cutting edge for RMIT , and a thinner, simple sans-serif font for the rest. The text color is going to be red, and the color of the curves/ellipses should be complementary to red to highlight the texts.

My first intention was to recreate the water ripple effect. The idea was inspired by the interactive koi pond wallpaper, in which you tap your screen and the water ripples and the fish would swim away.  My lack of experience with Javascript had me doing some research for what can be achieved with JS, and the first thing that came up was the [Perlin Noise Flow Fields](https://www.youtube.com/watch?v=sZBfLgfsvSk&list=LL&index=6&t=13s). 

<iframe width="600" height="550" src="https://editor.p5js.org/arthurrc/full/Bya9WiAnm"></iframe>

However, I didn’t want to just copy someone’s code, I wanted to actually understand my code, therefore, I opted for something simpler and would study more on Perlin Noise later. After that, I found a guide for creating the [Moire Pattern](https://www.youtube.com/watch?v=62SbexSgQIw&list=LL&index=4). It was perfect because it had what I originally wanted for my design, and I could understand what I was doing. In the video, the ellipse would go across the screen, but I wanted to go for something more complex: I wanted to recreate the bouncing DVD logo.

<iframe width="576" height="366" src="https://editor.p5js.org/sturrpzz/full/qWj_CTWlw"></iframe>

After some testing and research, I managed to create the bouncing effect.

After managing to make the ellipse strokes change color every time the ellipse hits the border, I decided to add another rectangle with a different color changing effect applied. As the ellipse only changes color every time it hits the border, the rectangle strokes change color every frame. I also wanted to have the rectangle rotate around itself.
