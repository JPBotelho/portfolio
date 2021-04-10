---
layout: default
title:  "Visual Effects"
date:  2019-08-09 20:55:40 +0800
categories: jekyll update
thumbnail: /assets/images/VFXThumb.PNG
thumbnail2: /assets/images/Camo1.png
thumbnail3: /assets/images/DissolveThumb.gif

projectNR: "5 Projects"
---

<script async defer src="https://buttons.github.io/buttons.js"></script>



# Index
* TOC
{:toc}

---

## Health Bar

<div markdown="0" class = "tagContainer">
<a href="#" class = "unityTag">Unity3D</a>
<a href ="#" class = "hlslTag"> HLSL</a>
</div>

![Test]({{ site.url }}{{ site.baseurl }}/assets/images/AnimatedBar.gif "Image")

I made this health bar in a 48-hour Gamejam called Gamesforgood. Read more about the game [here]({{site.baseurl }}{% post_url 2021-03-28-Games %}#fome-de-vencer-hunger-to-win).

It has a scrolling texture and the color changes from green to red as your life depletes; it is very simple in theory and implementation but it is a practical example of actually using shaders in the real world rather than to keep in your github and put in your portfolio. Displayed above. In my portfolio.

![Test]({{ site.url }}{{ site.baseurl }}/assets/images/FomeDeVencer2.png "Image")


---

## Procedural Toon Shader  <a href="https://github.com/JPBotelho/Procedural-Toon-Shader" class = "githubLink">see on github</a>

<div markdown="0" class = "tagContainer">
<a href="#" class = "unityTag">Unity3D</a>
<a href ="#" class = "hlslTag"> HLSL</a>
</div>

{% include githubStar.html content="https://github.com/JPBotelho/Procedural-Toon-Shader" %} 

Swaps a linear lighting function with a non-linear one for a stylized look.

A normal lighting function usually returns a linear value from 0 to 1. This implementation takes that value and uses it as the input to a custom, non-linear function set by an Animation Curve element in the Unity Engine. It allows for the creation of "steps" in the lighting, where areas of similar illumination are attributed the same value, giving it a more cartoony look.

{:refdef: style="text-align: center;"}
![Test]({{ site.url }}{{ site.baseurl }}/assets/images/ProcToonShader.png "Image")
{: refdef}

----



## Camouflage Shader <a href="https://github.com/JPBotelho/Camouflage-Shader" class = "githubLink">see on github</a>

<div markdown="https://github.com/JPBotelho/Fractal-Megacollection" class = "tagContainer">
<a href="#" class = "unityTag">Unity3D</a>
<a href ="#" class = "hlslTag"> HLSL</a>
</div>

{% include githubStar.html content="https://github.com/JPBotelho/Camouflage-Shader" %} 


Applies a camouflage texture based on a pre-defined map.

This is a very simple shader but can allow for some pretty cool customization. It takes a black/white map, with camouflage being rendered where it is white. 

{:refdef: style="text-align: center;"}
![Test]({{ site.url }}{{ site.baseurl }}/assets/images/Camo2.png "Image")
![Test]({{ site.url }}{{ site.baseurl }}/assets/images/Camo1.png "Image")
{: refdef}

---


## Dissolve Effect <a href="https://github.com/JPBotelho/Dissolve-Shader" class = "githubLink">see on github</a>

<div markdown="0" class = "tagContainer">
<a href="#" class = "unityTag">Unity3D</a>
<a href ="#" class = "hlslTag"> HLSL</a>
</div>

{% include githubStar.html content="https://github.com/JPBotelho/Dissolve-Shader" %} 

Makes an object progressively transparent based on a noise map.


{:refdef: style="text-align: center;"}
![Test]({{ site.url }}{{ site.baseurl }}/assets/images/Dissolve.gif "Image")
{: refdef}

---


## Triplanar Mapping <a href="https://github.com/JPBotelho/Triplanar-Mapping" class = "githubLink">see on github</a>

<div markdown="0" class = "tagContainer">
<a href="#" class = "unityTag">Unity3D</a>
<a href ="#" class = "hlslTag"> HLSL</a>
</div>

{% include githubStar.html content="https://github.com/JPBotelho/Triplanar-Mapping" %} 

Allows for axis-based coloring and texturing, allowing, for example, to fake snow on top of an object.

{:refdef: style="text-align: center;"}
![Test]({{ site.url }}{{ site.baseurl }}/assets/images/Triplanar.png "Image")
{: refdef}

---






