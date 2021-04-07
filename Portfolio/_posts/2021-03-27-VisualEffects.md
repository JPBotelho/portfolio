---
layout: default
title:  "Visual Effects"
date:  2019-08-09 20:55:40 +0800
categories: jekyll update
thumbnail: /assets/images/VisualFXThumb3.png
projectNR: "5 Projects"
---

<script async defer src="https://buttons.github.io/buttons.js"></script>



# Index
* TOC
{:toc}

---

## Health Bar
![Test](/assets/images/AnimatedBar.gif "ageag")

I made this health bar in a 48-hour Gamejam called Gamesforgood. Read more about the game [here]({% post_url 2021-03-28-Games %}#fome-de-vencer-hunger-to-win).

It has a scrolling texture and the color changes from green to red as your life depletes; it is very simple in theory and implementation but it is a practical example of actually using shaders in the real world rather than to keep in your github and put in your portfolio. Displayed above. In my portfolio.

![Test](/assets/images/FomeDeVencer2.png "ageag")


---

## Procedural Toon Shader
#### [Github](https://github.com/JPBotelho/Procedural-Toon-Shader)
{% include github-star.html content="https://github.com/JPBotelho/Procedural-Toon-Shader" %} 

Swaps a linear lighting function with a non-linear one for a stylized look.

A normal lighting function usually returns a linear value from 0 to 1. Thins function takes that value and uses it as the input to a custom, non-linear function set by an Animation Curve element in the Unity Engine. It allows for the creation of "steps" in the lighting, where areas of similar illumination are attributed the same value, giving it a more cartoony look.

{:refdef: style="text-align: center;"}
![Test](/assets/images/ProcToonShader.png "ageag")
{: refdef}

----



## Camouflage Shader
#### [Github](https://github.com/JPBotelho/Camouflage-Shader)
{% include github-star.html content="https://github.com/JPBotelho/Camouflage-Shader" %} 


Applies a camouflage texture based on a pre-defined map. 

{:refdef: style="text-align: center;"}
![Test](/assets/images/Camo2.png "ageag")
![Test](/assets/images/Camo1.png "ageag")
{: refdef}

---


## Dissolve Effect
#### [Github](https://github.com/JPBotelho/Dissolve-Shader)
{% include github-star.html content="https://github.com/JPBotelho/Dissolve-Shader" %} 

Makes an object progressively transparent based on a noise map.


{:refdef: style="text-align: center;"}
![Test](/assets/images/Dissolve.gif "ageag")
{: refdef}

---


## Triplanar Mapping
#### [Github](https://github.com/JPBotelho/Triplanar-Mapping)
{% include github-star.html content="https://github.com/JPBotelho/Triplanar-Mapping" %} 

Allows for axis-based coloring and texturing, allowing for example, to fake snow on top of an object.

{:refdef: style="text-align: center;"}
![Test](/assets/images/Triplanar.png "ageag")
{: refdef}

---






