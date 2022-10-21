---
layout: post
tags: ["robotics","python", "internship"]
title: "JPL M2020 Internship"
date: 2022-08-20T20:46:38-07:00
math: false
draft: false
---

I worked in Section 374K with Justin Huang implementing RRTConnect has a motion
planning algorithm for the the 5 DOF arms on the Mars rovers. Usually in motion
planning, paths are smoothed to make corners into curves for less jerky motion;
however, for space robotics, planners try to send the least amount of data
through space to the rovers so the minimal number of viapoints is preferred. So
instead of smoothing the RRT-generated paths, I spent the majority of my time
simplifying the paths to the smallest number of viapoints.


My Final Presentation:

{{<gslides src="https://docs.google.com/presentation/d/144yxsp2Gmq1xHnJizLaELDZvPcQFjyscRQH1uQoaNi0/embed?start=false&loop=false&delayms=3000">}}

My Final Report, which has more information on path simplification algorithms:

{{<gslides src="https://drive.google.com/file/d/17RjiFg9-UV41khwbL1GnLTmD5a8BRGVz/preview">}}

I also got to hang out in the Mars Yard, where I got to see replicas of
Curiosity and Perserverence used to test out new features.

![percy](/images/percy.jpg)
