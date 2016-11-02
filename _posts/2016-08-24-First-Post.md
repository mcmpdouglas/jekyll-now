---
layout: post
title: News About My Projects in the Microscopy Facility
---

For my first year at the facility, I've mainly worked on setting up the facility: moving the microscopes, setting up users fees, training the users, etc. Last winter, I've set up an OMERO server at the Douglas for image storage and remote analysis. 

My first goal was to make sure it would be useful for our slide scanner images (from an Olympus scanner). I've located and installed scripts that now allow the users to export their *.vsi files and crop them for easier analysis. 

Since then, I've been looking into extending the image treatment capabilities of the server. I'm currently looking into implementing simple analysis through ImageJ (mean intensity, cell counting) as well as integrating deconvolution and denoising scripts. 

For deconvolution, an old colleague suggested I try AIDA, the Adaptative Image Deconvolution Algorithm. I'm currently trying it out on some of our datasets before trying to implement it in OMERO later. For denoising, I've recently come accross CANDLE-J, an open-source ImageJ implementation of the CANDLE program that was written here in Montreal by Haider Khan (https://github.com/haiderriazkhan/CANDLE-J). This ImageJ plugin worked amazingly well on our two-photon datasets, so much that it could allow us to image a whole mouse brain in hours instead of days.

I'll post news here of my progress for these projects and news about the facility.

Étienne
