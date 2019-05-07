---
title: 'PixlBux'
subtitle: 'SaaS application for creating universal shoppable images'
date: 2018-07-10 00:00:00
icon: android
description: SaaS application for creating universal shoppable images
featured_image: '/images/PixlBux/pbCard.png'
---

<div class="center">
	<h1><i class="fab fa-android"></i> PixlBux</h1>
	<br>
	<img src="/images/PixlBux/logo.png" class="appIcon"/>
	<br>
</div>
<div class="gallery" data-columns="5">
	<img src="/images/PixlBux/1.png">
	<img src="/images/PixlBux/2.png">
	<!-- <img src="/images/PixlBux/3.png"> -->
	<img src="/images/PixlBux/4.png">
	<img src="/images/PixlBux/5.png">
    <img src="/images/PixlBux/6.png">
    <!-- <img src="/images/PixlBux/7.png">
    <img src="/images/PixlBux/8.png"> -->
</div>

### What is it

PixlBux is a SaaS affiliate marketing platform looking to create universally parsable shoppable images. If you're not aware of what a shoppable image is, it's when elements in an image are linkable to webstore or program. Each popular social media platform has there on, private, implementation of this.

---

### Our Goal

Our goal was to create an application and format such that we could create shoppable images across any platform. The platform would be targeting affiliate marketers as an easy way to create and share their shoppable images.

---

### Research & Development

PixlBux was a proof of concept with a lot of research behind it. There was a lot of considerations of the limitations and features of different platforms such as WeChat, Facebook, Instagram and Twitter. Ultimately no platform is interested in communicating on a standardized system (understandable for publicly traded companies with shareholder interests). We settled on QR after noting its popularity in the Asian markets, unfortunately they're not as widespread in North America.

---

### Technical Details

The B2B facing android application allows you to generate and add QR Codes to images either in a fixed white-space on the side of the image with color coded tags or free placed anywhere.

The background image is fixed with a dynamic "sticker" overlay in which the user can move, zoom, and rotate the "stickers" (QR codes or color tags). Upon saving the sticker layer is drawn onto the background image. There was a lot of learning that came along with the graphics work ultimately leading me to start my own image editing and processing iOS application, [Deep Fried](/project/deep-fried).