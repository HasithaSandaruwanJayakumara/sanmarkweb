---
post_id: 84
title: 'Digitalised Sanmark Year-End Party welcome Project'
date: '2023-01-13T08:57:09+00:00'
author:
    - "Hasini Chamali"
layout: post
permalink: /digitalised-sanmark-year-end-party-welcome-project/
post_image: /assets/img/blog/Digitalised-Sanmark-Year-End-Party-welcome-Project-Blog.webp
button: "Read More +"
width: "800"
height: "400"
categories:
    - Uncategorized
# seo
description : "Our team leveraged their expertise in the software field to plan an event that was both attractive and technologically advanced."
---

At Sanmark Solutions, we understand the importance of happy and productive employees. That’s why we prioritise showing our appreciation for their hard work and creating opportunities for them to come together as a team.

On December 23rd, we hosted our Annual Year-End Gathering at Hikka Tranz hotel in Hikkaduwa. The evening was a great success, thanks to the hard work of our organising team.

Our team leveraged their expertise in the software field to plan a “welcoming experience” that was both attractive and technologically advanced. The idea came from our project manager, Ranga, and the rest of the team supported him. And also our young associate software developer Chethana expertly navigated the project to its successful conclusion.

The team created a “welcoming experience” using a mobile app and digital guiding system.

Instead, we focused on creating a welcoming guest experience using a mobile app and digital systems.

Upon arriving at the event, guests were prompted to scan a QR code from their invitation. A mobile app then popped up with a personalised welcome message and instructions. A nearby screen displayed a welcome message, a photo of the guest, and the designation of the guest. An audio announcement provided further instructions, such as table number and location.

Each table was also outfitted with a self-powered, glass-covered decoration with LED lights. As guests scanned their QR codes, the decoration at their assigned table began to blink, guiding them to their seats.

The welcoming experience was enjoyable and seamless and created a memorable evening for all attendees.

## Project Architectural Diagram

![Project Architectural Diagram]({{ site.baseurl }}/assets/img/blog/Digitalised-Sanmark-Year-End-Party-welcome-Project-Middle-one.webp){:width="800" height="400" .img-fluid .w-100}

## Technical Process for Guests Welcoming

The technical process behind our Annual Year-End Gathering was carefully planned to ensure a smooth and personalised guest experience.

Upon arrival, guests were greeted with a Flutter app with a QR code Scanner, which scanned the QR code on their invitation and identified them by sending the data to the central Node JS server. This server stored all relevant data in a JSON file, serving as the mobile app’s database. Once the guest was identified, the server sent a personalised welcome message to the mobile app and sent relevant details to other WebSocket connections.

This process also included displaying the welcome message, image, and other details on a large screen via a projector connected to a PC. A similar message was also displayed on a nearby screen near the mobile app at the entrance.

All table indicators were connected to the central server and kept active with their lights always on. Once a guest scanned their QR code, the server sent a signal to the related table indicator, causing the NodeMCU to blink. At the same time, the central server sent signals to an audio streaming app, which converted the text into an audio announcement and welcomed the guest with their name and table number.

![Digitalised Sanmark Year End Party]({{ site.baseurl }}/assets/img/blog/Digitalised-Sanmark-Year-End-Party-welcome-Project-Middle-two.webp){:width="800" height="400" .img-fluid .w-100}

## Hardware Components Used

The technology behind our Annual Year-End Gathering’s welcome experience was crucial to its success. Our team utilised a variety of hardware components to create a seamless and engaging experience for guests.

- First and foremost, the mobile app that guests used to check in and receive instructions was run on a mobile phone.
- A laptop was also used to run the central server, which was run using Node Js.
- A multimedia projector was used to display the personalised welcome messages and images to the guest on a nearby screen.
- Five NodeMCUs were deployed to ensure seamless navigation for our guests. These compact and capable devices, connected wirelessly via WiFi, were instrumental in managing the lighting for the event.
- To power the NodeMCUs and table indicator LED lights, we used rechargeable batteries with 12v. Some electronic parts were also necessary for the proper functioning of the NodeMCUs.
{: .ml-5 .blog-list-disc }
  

These hardware components allowed us to create an unforgettable Cyber Heaven theme and ensure that guests were greeted with the personalised and technologically advanced experience they deserved.

## Technologies Used

- Websocket
- IOT programming
- Electronics
- Text to speech
- HTML
- File Based data storage
- Flutter
- JavaScript
- Node.js
{: .ml-5 .blog-list-disc }

## Further Possible Improvements

As with any event, there is always room for improvement. Our Annual Year-End Gathering was no exception.

- One potential improvement for future events would be to use more NodeMCUs to control the lighting throughout the location. This would allow us to create different ambiences and enhance the event’s overall atmosphere.
- Additionally, mobile or email notifications could be implemented by notifying the organiser or all members joining the event upon each guest’s arrival.
- Another interesting feature could be social media updates for new guest arrival, allowing the guests to check in and notify others that they are attending the event.
- There could also be options to connect cameras and capture the arrival of guests or take pictures to be used later on.
{: .ml-5 .blog-list-disc }

These are just a few possibilities, and technology is constantly advancing. Other options, such as face recognition, NFC cards, etc., could be explored instead of QR apps to improve the guest experience.

The Annual Year-End Gathering was a resounding success, thanks in large part to the meticulous organisation of our team. The event was truly amazing, and attendees were left impressed and satisfied with the overall experience. It was clear that much time and effort went into planning the event, and it paid off as an unforgettable evening for all.