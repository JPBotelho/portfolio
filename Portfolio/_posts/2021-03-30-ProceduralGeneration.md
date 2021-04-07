---
layout: default
title:  "Procedural Generation"
date:  2019-08-09 20:55:40 +0800
categories: jekyll update
thumbnail: /assets/images/ProcGenThumbnail.png
projectNR: "2 Projects"
---
<script async defer src="https://buttons.github.io/buttons.js"></script>

# Index
* TOC
{:toc}

---
## Unity Road Generator
#### [Github](https://github.com/JPBotelho/Unity-Road-Generator)
{% include github-star.html content="https://github.com/JPBotelho/Unity-Road-Generator" %} 

After toying with convex meshes and procedural low poly models, this was the next step in my procedural generation adventure. I found a half-working Catmull-Rom spline implementation in a random MIT licensed github repo and got to work. I cleaned up the code from there and used it to generate road meshes with curbs at the sides. It wasn't much in terms of innovation but it was an experience of code archeology and adaptation.

{:refdef: style="text-align: center;"}
![Test](/assets/images/ProcGenThumbnail.png "ageag")
![Test](/assets/images/RoadSpline.png "ageag")
{: refdef}

---

## Voxel Marching Cubes Terrain
#### [Github](https://github.com/JPBotelho/Voxel-Terrain)
{% include github-star.html content="https://github.com/JPBotelho/Voxel-Terrain" %} 

Voxel-generated terrain is something that has always fascinated me. For this project, I started off with [Scrawk's Marching Cubes](https://github.com/Scrawk/Marching-Cubes) implementation. The code uses a noise texture as a heightmap to populate an array of voxels, which are then meshed using Scrawk's code. Top faces are rendered with a different color according to its normal vector. 

{:refdef: style="text-align: center;"}
![Test](/assets/images/Terrain.png "ageag")
![Test](/assets/images/Terrain2.png "ageag")
{: refdef}


---
