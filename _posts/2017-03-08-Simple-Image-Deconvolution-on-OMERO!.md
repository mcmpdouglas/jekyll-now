---
layout: post
title: Simple Image Deconvolution on the OMERO server
---

![omdecon](/images/omdecon.png)

I finally finished writing the first version of **omdecon**, a simple way to deconvolute your images on the OMERO server. Using omdecon, you just select an image, start the script, and your deconvoluted images will soon be available in the same dataset! It's that simple!

This script uses a state-of-the-art open-source method, **[AIDA, the Adaptative Image Deconvolution Algorithm](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3166524/)**. All you need to use it is to supply a PSF, for example, an image of a bead,
and the script takes care of the rest. 

You will also probably need to remove the background from your image so omdecon can take care of that for you. Either enter a value to be subtracted from all planes or trace an ROI and let omdecon calculate the background value for each plane.

As an added convenience, I also included a simple way to produce theoretical PSFs using Christoph Gohlke's **[PSF module](http://www.lfd.uci.edu/~gohlke/code/psf.py.html)**. There's two different ways to use this module through omdecon:
 
**Manually set your PSF:** Enter all the information about your experiment, such as the technique and the different channels you used.
  
**Automatically set your PSF:** For this, your images will have to be tagged with the proper metadata:
  - Objective name (from which omdecon deduces immersion medium and technique used)
  - Numerical Aperture
  - Channel excitation and emission

To use it, go to the scripts menu in OMERO and click on "Deconvolution". You will find the omdecon script there.

Please read the instructions that come with omdecon before using it! 

Keep me posted if you use it!

![omdecon interface](/images/omdecon_interface.png)
