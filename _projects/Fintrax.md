---
title: 'Fintrax'
subtitle: 'The first ever iOS application used operationally worldwide supporting all air mobility squadrons within the Royal Canadian Air Force'
icon: apple
date: 2018-07-13 00:00:00
description: The first ever iOS application used operationally worldwide supporting all air mobility squadrons within the Royal Canadian Air Force.
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
### Overview

The Royal Canadian Air Force (RCAF) runs many missions moving resources around the world. These missions involve a plethora of paperwork for each crew member and the aircraft itself. FinTrax is a data and expense tracking application designed to be used in flight on these missions to save the crew time and energy. It tracks everything from aircraft expenses and services to crew expenses and per diems. This is app is internal to the RCAF and cannot be found on the App Store.

If you want to know more, I go in depth in my article [here](https://medium.com/@barbulescualex/my-experience-working-for-the-royal-canadian-air-force-as-an-ios-developer-c188d67b136c).

---

### My Role

I was the **lead iOS developer** on this project in a team of 5. I found myself in a technical leadership position by virtue of being the only person with iOS development experience. I worked alongside 2 full stack developers (one of them being our team's lead), a UX/UI designer and a business developer. 

### Translating User Requirements

There was quite a large discovery phase of the project, we had went to the Trenton Air Force Base twice to interview service memebers (anybody from pilots to finance) about what they would like to see in the application. Coming up with a solid structure for the application, especially a solid data model, was imperative before we began the software development.

Unsurprisingly, as the app progressed, so did our notion of what the user requirements were. The more people tested the app out, the more the requirements changed and grew. 

### Code Architecture
I took ownership of the code base, architecture and code style decisions. We had went with hybrid MVC architecture revolving around our Core Data model. The decision to go with an MVC style architecture was simple, my SWE co-workers were both rails developers, so keeping the app to a well understood architecture allowed for easier onboarding into the project.

### Task Delegation
Handling the main branch meant I needed to do code reviews and task delegation. For every release iteration (alpha -> beta -> 1.0.0 -~-> 1.2.0), we would get together and open up issues in github assigning priorities, milestones and who's responsible for it. Having time constraints for every release iteration meant having to choose the most important bugs/features. 

