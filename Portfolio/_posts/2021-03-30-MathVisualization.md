---
layout: default
title:  "Mathematical Visualization"
date:  2019-08-09 20:55:40 +0800
categories: jekyll update
thumbnail: /assets/images/MathVizThumbnail.png
projectNR: "7"
---
<script async defer src="https://buttons.github.io/buttons.js"></script>

Maths, although often boring, can produce some very interesting and pretty images. In this section, I display my implementations of concepts that I found interesting and try to explain them in laymans terms, so that the next person without math knowledge that comes along can understand and implement it. I imagine these repositories not as something to download and run, but as something to consult and draw ideas from. It was the way I implemented many of these - hop from site to site, blog to blog hoping to get just a hint as to how I should implement something. I hope this website can also serve as one of these sources of knowledge and reference. At the very least, it serves as a trippy art gallery.

Note: my english in these explanation posts somewhat reads like a russian trying to speak english for the first time. I think it gets the main point across without the useless and distracting embelishments of writing with proper styling and grammar.

# Index
* TOC
{:toc}

---
## 2D Fractals
#### [Github](https://github.com/JPBotelho/Fractal-Megacollection)
{% include github-star.html content="https://github.com/JPBotelho/Fractal-Megacollection" %} 


Implementation of the following fractal formulas:
 - Mandelbrot   
 - Multibrot 
 - Julia
 - Multijulia
 - Burning Ship
 - Tricorn
 - Barnsley Fractal
 - Magnet Fractal
 - Newton Fractal w/ Transformation Vector
 - Burning Julia
 - Conjulia

And the following rendering techniques:
 - Escape-Time
 - Smooth
 - Lyapunov Exponent
 - Orbit Trap
 - Pickover Stalk
 - Edge Detection
 - Normal Mapped
 - Hue
 - Cheap Interior Distance Estimation

2D fractals are simple to implement. For every pixel on your screen, create a complex number given by x+iy. Pass that number into a function. In the case of the mandelbrot set, (Z^2)+1. If the result is bigger than 4, it will explode in the next iterations and go bigger than infinity. In that case, it does not belong in the set. If it is not bigger than 4, take that result and put it in the function over and over again. If it doesn't escape after a certain nr of iterations, it is safe to say that it belongs. The higher these iterations the more detailed your set will be.

Important: Do not forget the function (Z^2)+1 is a complex function, and Z is initialized to x+iy. You must implement the proper exponent function.

{:refdef: style="text-align: center;"}
![Test](/assets/images/MathVizThumbnail.png "ageag")
![Test](/assets/images/Mandelbrot1.png "ageag")
![Test](/assets/images/Barnsley2.png "ageag")
{: refdef}


---


## Raymarched Fractals
#### [Github](https://github.com/JPBotelho/Raymarched-Fractals/)
{% include github-star.html content="https://github.com/JPBotelho/Raymarched-Fractals" %} 

First experimentation with Raymarching. Implemented in Unity as a Post-Processing effect. The Signed Distance Functions were taken from Shadertoy, and for the rendering it is a mixture of fake iteration-based Ambient Occlusion and Phong shading.

Raymarching works by shooting a ray out of your camera through every pixel on your screen. Then, you have a function that tells you the distance from any point to the object you want to render (it can be any shape, even these fractals, it depends on the function!). What you do then is you go forward by the distance to the object. If after the step the distance is tiny, you have touched the object. If not, keep going. Eventually you will either hit the object in which case you can render it, for example, by the nr of iterations, or you haven't, and you just draw background.

The function that gives you the distance to the object is called an SDF, or signed distance function. If you search for them on, for example, shadertoy, you can find many. They are usually in a function called map(), which incorporates multiple of these SDFs into a single function, in order to render multiple objects at the same time.

Q: How do you not hit the object at every step? You are moving the distance to it every time!

A: You can pass next to the object. Even though you are close to it, you never hit it. See: [Reference](https://viclw17.github.io/2018/11/29/raymarching-algorithm/)

![Test](/assets/images/RaymarchedFractals2.png "ageag")

{:refdef: style="text-align: center;"}
### ![Test](/assets/images/RaymarchedFractal.gif "ageag")
{: refdef}

---

## Buddhabrot
#### [Github](https://github.com/JPBotelho/Buddhabrot)
{% include github-star.html content="https://github.com/JPBotelho/Buddhabrot" %} 

Mandelbrot set variants rendered with a histogram.

A Mandelbrot set is rendered by repeatedly applying a function to your pixel coordinates and seeing if the values go to infinity.

Start at Z(x + iy), and repeat (Z^2)+1

If a point goes to infinity, it doesn't belong in the set. 
To render a Buddhabrot, you take every point that does not belong in the set (escaped to infinity) and see what points they visited. How? At every step, after applying the function, you see where your point is in the image. Increase the value of those coordinates by 1. Repeat that until it escapes. 
After you do this for every point, you will have a histogram that tells you how many times a pixel was visited by the function, which you can render as, for example, grayscale.

![Test](/assets/images/Tricorn.png "ageag")
![Test](/assets/images/Buddhabrot3.png "ageag")

---

## Knots
#### [Github](https://github.com/JPBotelho/Knots)
{% include github-star.html content="https://github.com/JPBotelho/Knots" %} 

Generation and triangulation of mathematical knots.

Knots are defined by a function that gives you a Point(x, y, z) from a single variable.
That variable normally starts at -π and goes to π. You go slowly from the start to finish, maybe incrementing 0.01 every step, and you sample the functions that give you the point. This will gives you all the points in the knot.

For triangulating it, you generate the normal using one point of the knot and the next. Then, imagine a circle aligned with that normal, like a tube around the knot. Generate n points evenly in that circle, and do that at every point. Those are your vertices. Triangulate.

{:refdef: style="text-align: center;"}
![Test](/assets/images/Knot1.png "ageag")
![Test](/assets/images/Knot3.png "ageag")
{: refdef}

---

## Lorenz System
#### [Github](https://github.com/JPBotelho/Lorenz-System)
{% include github-star.html content="https://github.com/JPBotelho/Lorenz-System" %} 

Visualization of a Chaotic 3 variable system with a histogram.

The lorenz system is a set of 3 equations that tell you how the X, Y, Z coordinates of a point will change over time. These 3 equations have 3 fixed variables: ρ, σ , β, which are fixed at the start. For example, ρ = 28, σ = 10, and β = 8/3.
You start at point like P(0.1, 0, 0) (It cannot be all 0s, because otherwise it would never change). Then you apply these functions over and over again, adding a little bit of time each time you do so (0.01). The smaller the timestep the more precise your result will be, since there is less time for the point to move.
Then, calculate where in the image your point is. Increment that pixel. In the end, after X iterations, you get a histogram where every pixel knows how many times it was visited, you can just render it as grayscale.

{:refdef: style="text-align: center;"}
![Test](/assets/images/Lorenz1.png "ageag")
![Test](/assets/images/Lorenz2.png "ageag")
{: refdef}
---

## Mobius Strip
#### [Github](https://github.com/JPBotelho/Mobius-Strip)
{% include github-star.html content="https://github.com/JPBotelho/Mobius-Strip" %} 

2 Variable parametric surface plotting and triangulation.

A Mobius Strip is a one-sided surface. If you keep going forward in one, you will be on the other side without having crossed an edge. It can be rendered using as a parametric surface: Imagine you have a plane (u, v), going from u [0; 2π[ and v [-1; 1].

Given a point in this plane, the parametric surface equations will tell you where it will end up in three dimensions. so from P(u,v) you get P(x,y,z). It is essentially a deformation of the plane. In order to render it, generate a grid that will correspond to your plane. Triangulate it, and then calculate the transformed position for every vertex. The vertices will change place but the triangles will remain the same.

{:refdef: style="text-align: center;"}
![Test](/assets/images/Mobius.png "ageag")
![Test](/assets/images/Mobius2.png "ageag")
{: refdef}
---

## Cellular Automata
#### [Github]()
Simulation of individual cell behaviour being based on collective status.
{:refdef: style="text-align: center;"}
![Test](/assets/images/CellularAutomata.png "ageag")
{: refdef}

---