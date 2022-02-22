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
    <h3>WWDC 2019 Student Scholarship Submission</h3>
    <h4>Metal | Accelerate | AVFoundation</h4>
	<br>
	<a href="https://github.com/barbulescualex/BeatMatch" class="buttonBlue button--large">GitHub</a>
    <br>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/7e6X7DzddIQ" frameborder="0" allowfullscreen></iframe>
</div>

### Overview

BeatMatch is an audio visualization game relying on signal processing and metal shaders. This was my 2019 WWDC Student Scholarship submission. While I did not get accepted, I did secure my first internship at Apple shortly after.

<img src="/images/BeatMatch/visulizerDemo.gif"/>

---

<!-- ### Audio Visualization - A Speed Tutorial

The sound goes through the `AVAudioEngine` class where a tap is inserted to get the buffer data. From there we can calculate the uniform inputs for our metal shaders.

**Current Audio Volume**

This is for the bumping circle, doing a RMS calcultion and linear interpolation will get us smooth values for each draw cycle.

**Frequency Magnitudes**

This is a more complicated task but essentially we do a Fast Fourier Transform to get the intensity in frequency bins, chop of the imaginary part and normalize the values.

--- -->

### Tutorials
Expanding on what I learned by doing this project, I've created multiple tutorials directly related to this. In fact, pretty much all my tutorials touch the GPU in one way or another.

The following tutorials were direct spawns of this project:

1. [Using Swift Playgrounds & Playground Books](https://medium.com/@barbulescualex/using-swift-playgrounds-playground-books-87c2707be2b5)
2. [Making Your First Circle Using Metal Shaders](https://medium.com/@barbulescualex/making-your-first-circle-using-metal-shaders-1e5049ec8505)
3. [Audio Visualization in Swift Using Metal and Accelerate (Part 1)](https://betterprogramming.pub/audio-visualization-in-swift-using-metal-accelerate-part-1-390965c095d7)
4. [Audio Visualization in Swift Using Metal and Accelerate (Part 2)](https://betterprogramming.pub/audio-visualization-in-swift-using-metal-accelerate-part-2-7ec8df4def91)