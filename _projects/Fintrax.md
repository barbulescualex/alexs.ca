---
title: 'Fintrax'
subtitle: 'The first ever iOS application used operationally worldwide supporting all air mobility squadrons within the Royal Canadian Air Force'
icon: apple
date: 2018-07-13 00:00:00
description: Board is a stylish full-width masonry grid theme. Made for designers, artists, photographers and developers to show off their best work.
featured_image: '/images/FinTrax/fintraxCard.png'
---

<div class="center">
	<h1><i class="fab fa-apple"></i> FinTrax</h1>
    <br>
    <img src="/images/FinTrax/logo.png" class= "roundedAppIcon"/>
	<br>
	<p>The first ever iOS application used operationally worldwide supporting all air mobility squadrons within the Royal Canadian Air Force</p>
</div>

<div class="gallery" data-columns="1">
	<img src="/images/FinTrax/1.png" class = "height">
	<img src="/images/FinTrax/2.png" class = "height">
	<img src="/images/FinTrax/3.png" class = "height">
</div>
### What is it

FinTrax is a data and expense tracking application designed to be used in flight on air mobility missions. It tracks everything from aircraft expenses and services to crew expenses and per diems. 

If you want to know more, I go in depth in my article here.

---

### My Role

I was the **lead iOS developer** on this project in a team of 5. How did I find myself in the leadership position for the project? Simply I was the only iOS developer, so technically I'm not being misleading in my claim to be the "lead". I worked alongside 2 full stack developers (one of them being our team's tech lead), a UX/UI designer and a business developer. 

There was quite a large discovery phase of the project, we had went to the Trenton Air Force Base twice to interview service memebers (anybody from pilots to finance) about what they would like to see in the application. Coming up with a solid structure for the application, especially a solid data model, was imperative before we began the software development.

In theory we had started the software development with a "solid plan" and "solid data model", as we soon came to learn every squadron needed slightly different functionality and leading to about 5-6 big refactors in the data model.

##### Code Architecture
I took ownership of the code base, architecture and code style decisions. We had went with hybrid MVC architecture revolving around our Core Data model. The decision to go with an MVC style architecture was simple, my SWE co-workers were both rails developers, so keeping the app to a well understood architecture allowed for easier onboarding into the project.

##### Task Delegation
Handling master meant I needed to do code reviews and task delegation. For every release iteration (alpha -> beta -> 1.0.0 -~-> 1.2.0), we would get together and open up issues in github assigning priorities, milestones and who's responsible for it. Having time constraints for every release iteration meant having to choose the most important bugs/features. 

As the project manager I also had to decide if I should partition a task to a co-worker, or do it myself. As the sole iOS developer this was a difficult process. Do I handle this complicated task myself knowing I can complete it faster or do I empower my coworkers and create a more inclusive development environment?

