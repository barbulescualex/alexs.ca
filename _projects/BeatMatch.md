---
title: 'BeatMatch'
subtitle: 'Audio visualization playground built with the Metal, Accelerate and AVFoundation frameworks'
icon: apple
date: 2018-07-12 12:00:00
description: Audio visualization playground built with the Metal, Accelerate and AVFoundation frameworks.
featured_image: '/images/BeatMatch/BeatMatchCard.png'
---

<div class="center">
    <img src="/images/BeatMatch/logo.png">
    <h2><i class="fab fa-apple"></i> Swift Playground Book</h2>
    <h4>Metal | Accelerate | AVFoundation</h4>
	<br>
	<a href="https://github.com/barbulescualex/BeatMatch" class="buttonBlue button--large">GitHub</a>
    <br>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/7e6X7DzddIQ" frameborder="0" allowfullscreen></iframe>
</div>

### What is it

BeatMatch is an audio visualization game relying on signal processing and metal shaders. 

<img src="/images/BeatMatch/visulizerDemo.gif"/>

---

### Audio Visualization - A Speed Tutorial

The sound goes through the `AVAudioEngine` class where a tap is inserted to get the buffer data. From there we can calculate the uniform inputs for our metal shaders.

**Current Audio Volume**

This is for the bumping circle, doing a RMS calcultion and linear interpolation will get us smooth values for each draw cycle.

**Frequency Magnitudes**

This is a more complicated task but essentially we do a Fast Fourier Transform to get the intensity in frequency bins, chop of the imaginary part and normalize the values.

---

### Tutorials
I'm currently working on making tuturials out of all the things I've learned. Mainly Metal Shaders and signal processing. The list below will be updated as they come :).

1. [Using Swift Playgrounds & Playground Books](https://medium.com/@barbulescualex/using-swift-playgrounds-playground-books-87c2707be2b5)
2. [Making Your First Circle Using Metal Shaders](https://medium.com/@barbulescualex/making-your-first-circle-using-metal-shaders-1e5049ec8505)