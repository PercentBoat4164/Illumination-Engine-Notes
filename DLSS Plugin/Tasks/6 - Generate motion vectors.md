- [ ] #colin Generate motion vectors on the URP
## Assignee - Colin McVety

Useful links - 
https://en.wikipedia.org/wiki/Motion_estimation
https://en.wikipedia.org/wiki/Deep_learning_super_sampling



Goal: Each frame, map each pixel of each object to its position in the previous frame as a 2D vector

What I need Colin to do: create the algorithm that calculates the vector for each pixel. 
What he needs to know: how to reference each pixel. This should come from pixel shaders
How to write shaders that work for vulkan (glsl, hlsl), directx (hlsl) (learn hlsl)
gl_FragCoord for glsl

The algorithm should take data from unity, generate the motion vectors, and send that data to dlss. In order for dlss to process it, it must be of format RG32_FLOAT or RG16_FLOAT

Unity uses object based motion vectors, we need per pixel motion vectors

http://john-chapman-graphics.blogspot.com/2013/01/per-object-motion-blur.html



https://docs.unity3d.com/ScriptReference/Camera.WorldToScreenPoint.html

find some place online to mess around with shaders

writing shaders 