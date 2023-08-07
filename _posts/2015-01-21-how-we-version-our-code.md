---
post_id: 2
title: 'How We Version Our Code'
date: '2015-01-21T08:47:14+00:00'
author: 
    - "Supun Budhajeewa"
layout: post
permalink: /how-we-version-our-code/
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
post_image: /assets/img/blog/how-we-version-our-code.webp
button: "Read More +"
width: "800"
height: "400"
categories:
    - Coding
    - English
tags:
    - Git
    - versionning
# seo
description : "Software versioning is the process of assigning either unique version names or unique version numbers to unique states of computer software. That is what Wikipedia says about versioning code. Here in Sanmark, we religiously version our code. Our versioning method is tightly fitted with our source control system, which is Git. It won&#8217;t be a [&hellip;]"
---

Software versioning is the process of assigning either unique version names or unique version numbers to unique states of computer software. That is what [Wikipedia says](http://en.wikipedia.org/wiki/Software_versioning){: target="_blank"} about versioning code. Here in Sanmark, we religiously version our code.

Our versioning method is tightly fitted with our source control system, which is Git. It won’t be a surprise that Git — and other tools of it’s kind — are called “version control systems” as well.

## A Little Bit About Our Git Usage

We follow a Git branching model that is close Gitflow method. We have a *master* branch, that will have only production ready code. Our *dev* branch is home to new completed features. We create *feature branches* off *dev* when we create new features. Our bug fix branches derive from *master branch*.

I hope to write more about our Git branching model in the next post.

## Version Numbering Method

Our version numbering method is very similar to that of [Semver](http://semver.org/){: target="_blank"}.

Version numbers contain three parts, in which the first is the *major version*, second is the *minor version*, and the third is the *patch version*.

Major version is only incremented when backword incompatible changes are made. Major versions can also include minor and patch changes.

Minor version is incremented when new features are introduced. Minor versions can also include patch changes.

Patch version is only incremented when bug fixes and other patches are added to the code.

### Versioning During Alpha and Beta Periods

During alpha period, we suffix our *Major.Minor.Patch* versions with “*-a-AlphaMajor.AlphaMinor.AlphaPatch*“.

So it’ll look like this:

```
Major.Minor.Patch-a-AlphaMajor.AlphaMinor.AlphaPatch
```
{:.pl-5}

```
1.0.0-a-1.4.9
```
{:.pl-5}


For beta, just replace “a” with a “b”.

The first released version our code will be “1.0.0-a-1.0.0” and it’ll increment from their.

## Git Tag and Commit Message

Once we decide upon a version number, we will use it as the commit message of the merge commit that merges the *dev* or *bug-fix* branch into *master*. Once merged, we will also put a tag to that merge commit with the same thing.