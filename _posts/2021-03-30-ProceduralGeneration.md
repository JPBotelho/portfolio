---
layout: default
title:  "Procedural Generation"
date:  2019-08-09 20:55:40 +0800
categories: jekyll update
thumbnail: /assets/images/ProcGenThumbnail.png
thumbnail2: /assets/images/VoxelTerrain.png

projectNR: "2 Projects"
---
<script async defer src="https://buttons.github.io/buttons.js"></script>

# Index
* TOC
{:toc}

---
## Unity Road Generator  <a href="https://github.com/JPBotelho/Unity-Road-Generator" class = "githubLink">see on github</a>
<div markdown="0" class = "tagContainer">
<a href="#" class = "unityTag">Unity3D</a>
<a href="#" class = "csharpTag">C#</a>
</div>

{% include githubStar.html content="https://github.com/JPBotelho/Unity-Road-Generator" %} 

After toying with convex meshes and procedural low poly models, this was the next step in my procedural generation adventure. I found a Catmull-Rom spline implementation in an obscure github repo and got to work. I cleaned up the code from there and used it to generate road meshes with curbs at the sides. It wasn't much in terms of innovation but it was an experience of code archeology and adaptation.

{:refdef: style="text-align: center;"}
![Test]({{ site.url }}{{ site.baseurl }}/assets/images/ProcGenThumbnail.png "Image")
![Test]({{ site.url }}{{ site.baseurl }}/assets/images/RoadSpline.png "Image")
{: refdef}

---

## Voxel Marching Cubes Terrain <a href="https://github.com/JPBotelho/Voxel-Terrain" class = "githubLink">see on github</a>
<div markdown="0" class = "tagContainer">
<a href="#" class = "unityTag">Unity3D</a>
<a href="#" class = "csharpTag">C#</a>
</div>
{% include githubStar.html content="https://github.com/JPBotelho/Voxel-Terrain" %} 

Voxel-generated terrain is something that has always fascinated me. For this project, I started off with [Scrawk's Marching Cubes](https://github.com/Scrawk/Marching-Cubes) implementation. The program uses a noise texture as a heightmap to populate a grid of voxels, which are then meshed using Scrawk's code. Top faces are rendered with a different color according to its normal vector. 

{:refdef: style="text-align: center;"}
![Test]({{ site.url }}{{ site.baseurl }}/assets/images/Terrain.png "Image")
![Test]({{ site.url }}{{ site.baseurl }}/assets/images/Terrain2.png "Image")
{: refdef}


---
