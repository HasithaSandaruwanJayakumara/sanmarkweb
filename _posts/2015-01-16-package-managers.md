---
post_id: 1
title: 'Package Managers: What are They and How are They Useful to Us?'
date: '2015-01-16T03:00:26+00:00'
author: 
    - "Supun Budhajeewa"
excerpt: '"Package Managers" are not new; but an year ago, we were not using them. It was kind of  an strange idea to us. But now we love them. This is the story of us at Sanmark adopting a couple of package managers and learning to love them!'
layout: post
permalink: /package-managers/
use_gradient_background_post:
    - 'no'
gradient_background_alternative_animation:
    - 'no'
qodef_content_behind_header:
    - 'no'
qodef_show_header_widget_areas:
    - 'yes'
qodef_standard_with_shape_appear_animation:
    - 'no'
post_image: /assets/img/blog/package-managers-post-image.webp
button: "Read More +"
width: "800"
height: "400"
categories:
    - Coding
    - English
tags:
    - Bower
    - Composer
    - 'Package Managers'
    - Ubuntu
# seo
description : "&quot;Package Managers&quot; are not new; but an year ago, we were not using them. It was kind of an strange idea to us. But now we love them. This is the story of us at Sanmark adopting a couple of package managers and learning to love them!"
---

“Package Managers” are not new; but an year ago, we were not using them. It was kind of an strange idea to us. But now we love them. This is the story of us at Sanmark adopting a couple of package managers and learning to love them!

## A Change in the Operating System

![](assets/img/blog/package-managers-middle-1.png){: .d-block}
In our beginning, Microsoft Windows was the only operating system used in the office. But that changed when I introduced Ubuntu to Kosala, our CEO. At the start, he was a little bit confused about doing things in Ubuntu, but he learned very quickly. He liked it so much so that he wanted to use Ubuntu as our “official operating system”.

Using that, our team soon had to realize installing — and updating, and removing — software doesn’t necessarily mean “Download. Double-click. Next. Next. I agree. Next. Next. Finish.”. Application software become parts of the OS itself, instead of things we forcibly make the OS co-operate with. We ask the OS to find, download, and install any software we want, and that’s it. OS will then go and find that software, check whether that needs any more software to work with (“dependencies”), download it with any dependencies, along with dependencies of dependencies and so on, and finally install the thing for us.

This was a huge change compared to Microsoft Windows we used to use, and I had a hard time explaining the advantages of this method over that of Windows.

## A Change in the Framework

![](assets/img/blog/package-managers-middle-2.png){: .d-block}

Last year we also started using Laravel as our PHP application development framework. This utilizes the PHP package manager “Composer”. Composer allows you to prepare a list of PHP Packages needed for your web application. Once done, Composer can download and install those packages in your application.

Composer is the second package manager that we got to work with.

## A Change in the Frontend

![](assets/img/blog/package-managers-middle-3.png){: .d-block}

Another thing we did in the last year is adopting the method of separating our web applications into to two clearly separate parts: the back-end (API) and the front-end (App). As mentioned above, Laravel became our API building framework. For the front-end, we chose AngularJS from the web-giant Google.

Having used to using Composer when developing applications in Laravel, we actively searched for a package manager that we can use when creating Javascript applications. We found a couple, but Bower from Twitter was the one we choose. Like Composer for PHP, Bower lets us prepare a list of needed packages and goes on to downloading and installing those packages inside our JS applications.

## Can I not Use Package Managers?

Of course you can! Although not-using a package manager in Ubuntu is a little bit difficult, you can easily not use package manager when building applications for PHP and Javascript.

### Ubuntu

Without asking Ubuntu’s package manager “apt-get”, you can browse Ubuntu’s package repositories manually through your web browser and download them. However, you will have to deal with identifying each package’s dependencies and downloading them as well.

Once you download them, you can use application “dpkg” to install them. But I am sorry to say that is more likely than not this process will fail.

### Composer

![](assets/img/blog/package-managers-middle-4.png){: .d-block}

Composer downloads the packages into your PHP application’s “vendors” directory. You can easily browse the web — Packagist and GitHub will be your favourite sources — for PHP packages, download them and put them in your “vendors” directory. You will have to check whether those packages have dependencies as well, because for them to work, they will need those dependencies installed.

### Bower

![](assets/img/blog/package-managers-middle-5.png){: .d-block}

It’s the same story as Composer. GitHub is full of Javascript packages that can be used in your applications. Have a great time hunting for dependencies here too. 🙂

## What are Package Managers then?

Package managers helps you find, install, keep them up-to-date, and remove any third-party packages on your Operating System or applications. They allow you to worry only about your OS or application, and they work to keep the third-party stuff managed.

## What are Dependencies?

Each third-party package is an application on their own, just like the one you are creating. They might be using other third-party packages to get their work done. They are called “dependencies” because the package you need installed depends on these other packages.

## Why do We Love Package Managers?

They make us feel super cool. 😀 No, really. We don’t have to upload a whole bunch of third party packages each time we deploy a web application. We just upload our own code along with a list of needed third party packages, and ask the package manager to download those stuff and get them installed. And that works like a charm. We avoid accidentally forgetting to upload some package because the only thing we have to upload is a little text file.

Apart from that, we can easily run “update” command to see whether any of our third party packages has new versions out there. Imagine trying to update third party packages in a half-a-dozen places manually. It’ll be a mess!

## So…

Package managers are cool and makes your work flow so much easier. They allow you to focus on your own code, rather than trying to keep up with some others’ packages. They make you so efficient!