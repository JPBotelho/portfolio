---
layout: default
title:  "Graphical Engines"
date:  2019-08-09 20:55:40 +0800
categories: jekyll update
thumbnail: /assets/images/EnginesThumbnail.png
projectNR: "2"
---
<script async defer src="https://buttons.github.io/buttons.js"></script>

# Index
* TOC
{:toc}

---

## [C# OpenGL Engine](https://github.com/JPBotelho/OpenGL-Sandbox)

It's my turn writing the typical OpenGL engine that everyone does. Except I did it in C#, which is the language I'm most comfortable with, as to not struggle with being unfamiliar with both the language and framework. This way, I was able to learn the basics of OpenGL without having to learn more advanced C++ at the same time.

It is rather crude, but it is enough to create a decent picture straight out of 2005. It has got:
- ASSIMP Model loading
- Directional Lights
- Point Lights
- Per light shadowmapping
- Skybox

Basically, it loads the standard scene everyone uses for rendering techniques and you can have a bunch of point lights in there and just have fun looking at them.

Here are some images:

![Test](/assets/images/OGL1.png "ageag")
![Test](/assets/images/OGL2.png "ageag")
![Test](/assets/images/OGL3.png "ageag")


---


## [DirectX Engine](https://github.com/JPBotelho/DirectX-Engine)

This was my first attempt at writing an engine and interacting with a graphics API, as well as using C++. I believe I tried to follow http://www.rastertek.com/tutdx11.html but quickly derailed. In the end, I got to the very beginning stage of an engine, having implemented an obj model loader and sucessfully implemented an icosphere. I quickly got demotivated for my lack of progress and autonomy, and put aside the project and engine-programming in general until my above attempt at an OpenGL engine.

I don't have many screenshots, because this barely rendered anything.
But I do have this icosphere:

{:refdef: style="text-align: center;"}
![Test](/assets/images/Ico.png "ageag")
{: refdef}


---

