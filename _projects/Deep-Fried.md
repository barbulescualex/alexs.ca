---
title: 'Deep Fried'
subtitle: 'The most popular deep fryer on the App Store!'
titleLink: 'https://deepfried.app'
icon: apple
date: 2018-07-14 00:00:00
description: The most popular deep fryer on the App Store!
featured_image: '/images/DF/dfCard.png'
---

<div class="center">
	<h1><i class="fab fa-apple"></i> Deep Fried</h1>
	<br>

	<img src="/images/DF/DeepFriedAppIcon.png" class="roundedAppIcon" />

	<h2>4.7/5 stars | 1200+ ratings</h2>
	<br>
	<a href="https://itunes.apple.com/us/app/deep-fried/id1436647902?mt=8&uo=4" class="button button--large red">Download</a>
	<a href="https://deepfried.app/" class="button button--large red">Visit Website</a>
</div>
<div class="gallery" data-columns="5">
	<img src="/images/DF/CameraPreviewX.png" class= "roundedImage">
	<img src="/images/DF/galleryX.png" class= "roundedImage">
	<img src="/images/DF/warpX.png" class= "roundedImage">
	<img src="/images/DF/editX.png" class= "roundedImage">
	<img src="/images/DF/saveX.png" class= "roundedImage">
</div>

---

### What is it

Deep Fried is an image editing and processing application. I'm the **sole developer and maintainer** of this application!

You can:

* Take fried images straight from your camera
* Warp images
* Add text
* Add custom assets
* Interact directly with your Deep Fried Meme folder in your camera roll

---

### Technical Details

As an image editing and processing application Deep Fried presented many technical hurdles to overcome. Developing novel features that nobody has done presented a lot of pain points.

#### Frameworks Used:
* MetalKit
* Core Image
* AVFoundation
* PhotoKit
* Core Data
* Firebasae (analytics tools)

Talking about each individual feature by itself is the easiest way to present the technical difficulties

---

#### Deep Fried Camera: AVFoundation | Core Image | MetalKit

Perhaps this is my most novel feature inside the application. I take buffer data in from the camera, apply the filters on the data and display it back to the screen in real time.

**GPU and CPU**

At first this process was very CPU intensive as I would be creating a CIImage from the buffer data to apply the filters (this takes place on the GPU through the Core Image framework) but then transforming it into a UIImage to display in an UIImageView on screen 30FPS. While this worked just fine the overall resource usage was very high. I then set out to optimize this by removing the need for the CPU to do work by displaying the data from the GPU directly from the screen. This led me into using the MetalKit framework, replacing the UIImageView with a MetalKit view. 

While this significantly cut down on my resource usage, I noticed older devices (pre  A10) could not handle the MetalKit view inside of my application. So for those devices I still use the CPU to display the processed camera feed.

**Initiating & Switching Cameras**

Unsuprisingly these processes can be very slow on the main thread. Moving these to background threads is mandatory (well not really, only if you want to provide a better user experience)

---

#### General Frying:

This is simply an extension of the Deep Fried camera (well this one actually came first). The only difference is instead of creating a CIImage from the buffer data I create it from the UIImage the user took/selected.

---

#### Warp Controller: Core Image

The warp controller allows you to bump, pinch and swirl images based on touch input. You can adjust the radius and intensity of the effect.

**Translating Touches**

This was the most annoying part of this feature by far, mainly because I tried to be lazy instead of actually doing some math. To effectively translate touches on an UIImageView holding an image into tangible coordinates (and radius of effect) for the *actual image* you need to know the pixel density difference of the screen vs image and figure out how it's sitting inside the UIImageView. (It would be nice if the UIImageView could provide this sort of information).

After calculating the density difference, some ratio math can let you know wether all the sides are touching the UIImageView (super rare) or wether the top/bottom or left/right is touching the UIImageView. From there you need to calculate the no touch zones.

After all that you need to remember that the UIImageView's origin point in its coordinate system is top-left while Core Image's origin is in the bottom-left.

---

#### Working With The Album And Collection View: PhotoKit

**Interacting With The User's Camera Roll**

At the root of my application resides the a UICollectionView which holds all the user's images from their album. I use a singleton class (yeah I know, sue me) to interact with the camera roll that instantiates the "Deep Fried Memes" folder if it doesn't exist, loads in thumbnails/full images, saves images, deletes images and fetches all the PHAssets.

**Populating the UICollectionView**

Buggy, slow, high memory usage. All things that can happen if you don't do this correctly. The saving grace is the PHCachingImageManager, this API handles most of the heavy lifting in terms of optimization. 

**Registering to PHPhotoLibraryDidChange**

PhotoKit sends out notifications like a mad man, if you're updating the collection view every time you get this notification you're wasting a lot energy. For this reason I using a flag "needsUpdate" that only gets set to true if the user leaves the application, deletes and image or saves an image.

---

#### Adding Text & Custom Assets To Your Images

Luckily I found an abandoned framework for this one. I updated it from Swift 3, fixed memory leaks and extended its functionality. Using Core Data I let users add in their own custom assets into the Edit controller and implemented fonts.
