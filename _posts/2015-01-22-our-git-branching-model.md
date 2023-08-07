---
post_id: 3
title: 'Our Git Branching Model'
date: '2015-01-22T09:26:41+00:00'
author: 
    - "Supun Budhajeewa"
layout: post
permalink: /our-git-branching-model/
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
post_image: /assets/img/blog/our-git-branching-model-post-image.webp
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
description : "Ah, Git, our one and only and lovable version controlling system! How would we have developed software without you? I want to share with you today the branching model we use here in Sanmark. As mentioned in the last post, our Git branching model is a little bit close to that of Gitflow. Initializing Project [&hellip;]"
---

Ah, Git, our one and only and lovable version controlling system! How would we have developed software without you?

I want to share with you today the branching model we use here in Sanmark. As mentioned in the [last post](/how-we-version-our-code/ "How We Version Our Code"){: target="_blank"}, our Git branching model is a little bit close to that of [Gitflow](http://nvie.com/posts/a-successful-git-branching-model/){: target="_blank"}.

## Initializing Project and Git Repository

We start with an empty directory and create the “.gitignore” file in it before doing anything else. Then we commit it as the “Initial Commit”.

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-1.webp){:.d-block}

Then two more branches are created, namely “dev” and “”init”.

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-2.webp){:.d-block}

It is this “init” branch we use to bootstrap our projects — project creation, configurations, compulsory package installation, environment setup all goes into this branch. Usually one person (Project Lead) handles this branch. He commits soon and often to this branch and get everything ready in a matter of an hour or two.

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-3.webp){:.d-block}

Once done, he’ll squash all the commits in the *init* branch into a single commit — of which’s commit message is often “Initiate project.”.

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-4.webp){:.d-block}

And then merge that to *dev* using fast-forward method. This “Initiate project.” commit will be the second commit of the *dev* branch (“Initial Commit” being the first.). After that, the *init* branch will be deleted.

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-5.webp){:.d-block}

Now the project and the Git repository is initialized. We can push the branches *master* and *dev* to a remote bare repository — either a manually maintained one, or one hosted in a Git hosting solution like GitLab and GitHub –, and other team members can clone this and start contributing to the project!

## Naming Feature and Bug-fix Branches

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-6.webp){:.d-block}

### Creating Branches for Issues Reported in Issue Tracker

If we are creating a feature or a bug-fix branch based on an issue in our issue tracker, we mention that issue’s number in our branch name. And we prefix our feature branch names with “do#” — bug-fix branch names are prefixed with “fix#”.

For an example, if we have a feature request with the number 123, and a bug report with the number 149, we will create a feature branch with the name “do#123” and a bug-fix branch with the name “fix#149”.

### Creating Branches without Issue Reports

If we are creating feature or bug-fix branches to do something that was not reported in the issue tracker, we prefix them with “do-” (for feature branches) or “fix-” (for bug-fix brances) and follow the prefixes with the actual name, which is written in camel-case. “do-create\_login\_system” and “fix-stop\_redirect\_loop” are examples.

## Creating Feature Branches

Feature branches will always branch-out from the *dev* branch. Before creating a new feature branch, we make sure we have the latest *dev* branch available (By fetching the *dev* branch from our remote central repository.). Once we confirm that we do have the latest *dev* branch, we create our feature branch from the last commit of that branch.

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-7.webp){:.d-block}

Then [*we commit early and often*]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-1.webp){:.d-block}

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-8.webp){:.d-block}

Once done, we squash all the commits of the feature branch into a single commit. We add a descriptive commit message for the squashed commit.

If we are squashing a branch created based on an issue from the issue tracker, we prefix the commit message with “#”, then the issue number, and finally the actual commit message (Eg. “#132 Create login system.”). If the branch was not based on a issue, just put the message without any prefixes.

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-9.webp){:.d-block}

And finally, we merge the feature branch into *dev* and delete the feature branch. Before doing that, we check whether *dev* branch has moved forward since we branched-out from it. If it hasn’t we go ahead and merge it.

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-10.webp){:.d-block}

### What if the *dev* Branch has Moved Forward?

If the dev branch has move forward since we branched-out, it’ll look like this after we fetch it just after we finish our feature-branch.

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-11.webp){:.d-block}

If this happens, we have to rebase our feature branch onto the latest *dev*.

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-12.webp){:.d-block}

Now we can fast-forward merge our feature branch into *dev*, and delete the feature branch.

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-13.webp){:.d-block}

## Creating Bug-fix Branches

Bug-fix branches are almost always branched-out from the *master* branch, unless the reported bug is not yet found in the code in the master branch, and only found in the *dev* branch — in which case the branch for fixing that bug will be branched-out from *dev*.

Changes are committed early and often, all commits are squashed into one at the end of the bug-fix process. The issue number should be a prefix in the commit message of the squash commit, if the branch was based on an issue from the issue tracker.

If the bug-fix branch was branched-out from *master*, it’ll be merged into both *master* and *dev* branches. Merge commits are created (Non-fast-forward merge method is used.).

If the bug-fix branch was branched-out from *dev*, it’ll be merged into the *dev* branch just like a feature branch.

## Merging into *master* Branch

Only production ready code will be merged to *master* branch. Only *dev* branch and bug-fix branches will be merged to *master* branch. Merges into *master* branch will always be non-fast-forward. Commit messages of the merge commits will be version numbers (Read the previous post “[How We Version Our Code](/how-we-version-our-code/ "How We Version Our Code"){: target="_blank"}“.).

![]({{ site.baseurl }}/assets/img/blog/our-git-branching-model-middle-14.webp){:.d-block}