Death Buther
- [x] #colin Provide a depth buffer for each frame [completion:: 2023-09-17 09:41:49]
- [x] #colin Provide color buffer for each frame [completion:: 2023-09-17 09:41:48]

Grab from Unity 
get Vulkan handle to the image

Can happen before other things

Resources - 
https://en.wikipedia.org/wiki/Z-buffering

https://developer.nvidia.com/content/depth-precision-visualized

https://www.geeksforgeeks.org/z-buffer-depth-buffer-method/
```
Algorithm :

First of all, initialize the depth of each pixel.
i.e,  d(i, j) = infinite (max length)
Initialize the color value for each pixel 
as c(i, j) = background color
for each polygon, do the following steps :

for (each pixel in polygon's projection)
{
    find depth i.e, z of polygon
    at (x, y) corresponding to pixel (i, j)
    
    if (z < d(i, j))
    {
        d(i, j) = z;
        c(i, j) = color;
    }
}
```

	