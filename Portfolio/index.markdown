---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
# [Engine Programming]()

# [Visual Effects]()

# [Mathematical Visualization]()

# [Procedural Generation]()

# [Other]()

{% highlight csharp %}
while(v <= 1)
{
    //vertices.Add(new Vector3(u, v, 0));
    uvs.Add(new Vector2(currX / (planeResolution-1), currY / (planeResolution-1)));
    //Instantiate(marker, new Vector3(u, v, 0), Quaternion.identity);
    float x = (1 + ((v / 2.0f) * Mathf.Cos(u / 2.0f))) * Mathf.Cos(u);
    float y = (1 + ((v / 2.0f) * Mathf.Cos(u / 2.0f))) * Mathf.Sin(u);
    float z = (v / 2.0f) * Mathf.Sin((u) / 2.0f);
    Vector3 position = new Vector3(x, y, z);
    vertices.Add(position);
    markers.Add(Instantiate(marker, position, Quaternion.identity));
    v += vStepSize;
    currY++;
}
{% endhighlight %}
