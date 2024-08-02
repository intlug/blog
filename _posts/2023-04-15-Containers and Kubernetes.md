---
layout: post
show_date: true
read_time: true
img: posts/stock/post-banner.jpg
title:  "Containers in a Kubernetes World"
description: Containers, how to use them and take advantage of Kubernetes
author: Peter Larsen
categories: presentation, containers, kubernetes, openshift
tags: [linux, monthly-talk]
toc: yes
github: intlug/blog
---

# Containers in a Kubernetes World

Date Recorded: April 1st, 2023
Recording: (TBD)[https://youtube.com]
Deck: [https://www.slideshare.net/plarsen67/containers-in-a-kubernetes-world]

# Containers are the new software distribution method

More than 10 years ago, Docker took a Linux feature (LXC) and make it easy to use. The result was a huge benefit to software development, and how we manage/host software on servers. Instead of using apt/yum/dnf/yast and similar tools to configure a host with proper software needed to run/support our application, we simply pull a container image that has everything needed to run.

Container images are independent of the host except for the kernel. It means we can run on the same Linux host applications made for different kinds of distributions, different releases of the same libraries etc. - the runtime compared to VMs are smaller, no OS overhead per container while still keeping each workload separate as if was a VM or different physical hardware. Containers has become so successful we have flatpak, appimages and similar formats to distribute graphical applications requiring X11/Wayland/GLX and other end-user access to devices. Allowing the maintainers of a project to make one single distributable instead of different ones per distribution and "fight" the dependency differences between every distribution.

No wonder developers and Linux admins flock to containers. But with scale, containers become complex and hard. What seems straight forward on a single host becomes a challenge when more than one host is needed to support workloads. Networking, storage, security, isolation, ingress, security and more must be shared/managed across all hosts allowing containers to "talk to one another" and be available to end users. This is what the Kubernetes project was created to do. A rewrite (upgrade?) of the Google BORG system that runs every Google workload as containers. Together with companies like Red Hat, Amazon Kubernetes quickly make Kubernetes.io into a FOSS project on the level of the Linux kernel. And as an industry, CNCF was created to standardize the container internals resulting in OCI.

