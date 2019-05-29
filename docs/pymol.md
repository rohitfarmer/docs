---
layout: default
title: Pymol
nav_order: 16
description: "Pymol"
---

# Pymol
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---
# Ray Tracing
```
set ray_trace_mode, 1 #this is for backborder
set antialias, 6; #higher the value smoother the picture is 
set ray_shadow, 1 #switch on the shadows
set ray_trace_gain, 0.0 #to alter the thickness of the outline
set cartoon_fancy_helices, 1 #for fancy cartoon
set cartoon_highlight_color, grey #to colour inside of helix
set ray_texture, 4 #it gives a matte style texture
ray 2400, 2400 #this is fore really high resolution image, you may not need it
```

*These are the two options I usually use: first one colours the inisde of helix as grey the second one doesn't*  

`set ray_trace_mode, 1; set antialias, 6; set ray_shadow, 1; set cartoon_highlight_color, grey;set ray_texture, 4`

`set ray_trace_mode, 1; set antialias, 6; set ray_shadow, 1; set ray_texture, 4`

*No black outline.*  
`set antialias, 6; set ray_shadow, 1; set ray_texture, 4 `

`ray`
