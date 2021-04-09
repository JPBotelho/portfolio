---
layout: default
title:  "Graphical Engines"
date:  2019-08-09 20:55:40 +0800
categories: jekyll update
thumbnail: /assets/images/EnginesThumbnail.png
projectNR: "2 Projects"
---
<script async defer src="https://buttons.github.io/buttons.js"></script>

# Index
* TOC
{:toc}

---

## C# OpenGL Engine <a href="https://github.com/JPBotelho/OpenGL-Sandbox" class = "githubLink">see on github</a> 

<div markdown="https://github.com/JPBotelho/Fractal-Megacollection" class = "tagContainer">
<a href="#" class = "csharpTag">C#</a>
<a href ="#" class = "openGLTag">OpenTK</a>
</div>

{% include github-star.html content="https://github.com/JPBotelho/OpenGL-Sandbox" %} 

This was my attempt at writing the typical OpenGL engine that everyone does. Except I did it in C# using OpenTK, which is the language I'm most comfortable with. I did this so I didn't have to learn the framework while learning C++. This way, I was able to learn the key concepts of rendering with OpenGL.

It is rather crude, but it is enough to create a decent picture straight out of 2005. It has got:
- ASSIMP Model loading
- Directional Lights
- Point Lights
- Per light shadowmapping
- Skybox

Basically, it loads Crytek Sponza and you can have a bunch of point lights in there and just have fun looking at them.

Here are some images:

![Test](/assets/images/OGL1.png "Image")
![Test](/assets/images/OGL2.png "Image")
![Test](/assets/images/OGL3.png "Image")


---


## DirectX Engine <a href="https://github.com/JPBotelho/DirectX-Engine" class = "githubLink">see on github</a>

<div markdown="0" class = "tagContainer">
<a href="#" class = "cppTag">C++</a>
<a href="#" class = "directXTag">DirectX 11</a>
</div>

{% include github-star.html content="https://github.com/JPBotelho/DirectX-Engine" %} 


This was my first attempt at writing an engine and interacting with a graphics API, as well as using C++. I believe I tried to follow [rastertek's tutorial](http://www.rastertek.com/tutdx11.html) but quickly derailed. In the end, I got to the very beginning stage of rendering, having implemented an obj model loader and sucessfully implemented an icosphere. I quickly got demotivated for my lack of progress and autonomy, and put aside the project and engine-programming in general until my above attempt at an OpenGL engine.

I don't have many screenshots, because this barely rendered anything.
But I do have this icosphere:

{:refdef: style="text-align: center;"}
![Test](/assets/images/Ico.png "Image")
{: refdef}


---

