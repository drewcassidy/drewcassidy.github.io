---
title: Making Realistic Particle Effects From Photos
tags: KSP restock gamedev 
---
While working on drills for ReStock I realized I needed some particle effects for when the drills are in use. I wanted the effect of small rocks being kicked up from the ground and falling back down, but my attempts at a texture for the rocks all ended up looking more like potatos. 

{% include figure-image.html
  float="right"
  src="potato-rock.png"
  caption="A lumpy excuse for a rock" %}

Here on earth, we have plenty of potato-shaped rocks due to erosion in water and wind, but in space theres no such forces to smooth out rocks, and they end up looking far more jagged, and dangerously so. Even small particles of lunar dust is razor sharp when viewed under a microscope.

Instead of hand-painting a realistic chunk of slag in photoshop I thought I would try creating it using photographs. Rocks are easy to come by, after all, so I grabbed a chunk of what I believe to be granite from outside. Photographing a real sample also has the benefit of allowing for easy flipbook animation of the particles, which KSP’s limitied particle system format luckly supports.

The setup is pretty simple. I used some mounting putty to hold the rock in 8 different angles, while I photographed it from above with my phone. I used an empty pringles can as a makeshift tripod to hold my phone in the same place for each shot with a fixed focus and exposure, and a stationary desk lamp slightly off-axis. I took 8 pictures total, rotating the rock about 45° each time. 

{% include figure-image.html
  src="setup-small.jpg"
  caption="The setup, using an empty pringles can as a tripod" %}

After the photos were taken, I imported them all into photoshop and masked out each one, arranged them into a 2x4 grid for the flipbook animation, and applied some color correction to make them the color I wanted. 

{% include figure-image.html
  src="flipbook.png" %}

I think the result looks pretty good, since the rocks appear to tumble as they are thrown arround, which breaks the illusion of them being flat billboards, which they are. 

{% include figure-video.html
  src="effects.mp4"
  caption="The effects in action" %}

Possible future additions to this technique:
- take 3 photos for each rotation with different lighting to make a normal map.
- use more photos for a more smooth animation
- rendering a spinning 3D model in blender instead of using photography

