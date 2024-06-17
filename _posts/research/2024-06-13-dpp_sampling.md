---
title: Dubbing Point Processes
excerpt: Live mixing soundscape fragments
tags:
- Media Art
- featured
author: santiagorenteria
#options: [minihead]
categories:
  - research
background-image: research.jpeg
icon: music
---

<div class="12u"><span class="image fit"><img src="{{ site.baseurl }}/images/dpp_sampling/uts-doc.JPG" alt="" /></span></div>

In this project I dubbed and remixed tape recordings from the <a href="https://slwa.wa.gov.au/stories/slwa-abc-radio/john-hutchinson-birdsong-collection">John Hutchinson's sound archive</a>. Hutchinson began this collection in 1959, when he accepted work with the Department of Agriculture. As such, this archive derives its sonic character from unique Western Australiian soundscapes spanning several decades and variegated geographies. I began exploring the archive manually, by ear, and listening to recordings that captured my attention. Eventually, I realised that I was not going to be able to go through the whole collection, which after a data analysis I confirmed had over 130 hours of soundscapes. Instead, I decided to implement a sampling mechanism that would allow me to extract an aural summary of the most interesting regions of the archive. You may think this as creating a thumbnail for sound, but instead of using compressed versions of digital images for fast browsing, I relied on stochastic point processes to sample sets of 1-second fragments with high diversity. Diversity was important because sampling uniformly at random yields less salient fragments. With this process in mind, I designed a bespoke interface to retrieve samples in real-time and mix them live before of an audience at the University of Technology Sydney as part of a research event at the Data Visualisation Institute.

<div class="12u"><span class="image fit"><img src="{{ site.baseurl }}/images/dpp_sampling/interface_screenshot.png" alt="" /></span></div>

So, how to quickly skim through a given audio collection without listening to it in full?

On the technical side, this is an application of determinantal point processes. Due to their ‘repulsive property’, owed to them being originally devised to model the spatial behaviour of fermions such as electrons, these stochastic processes have been <a href="https://dcase.community/documents/workshop2022/proceedings/DCASE2022Workshop_Outidrarine_34.pdf">recently proposed</a> as means to retrieve audio fragments with high sonic diversity. The peculiarity of this sampling process is that it enables the production of sets of 1-second fragments with contrasting sonic characteristics. Metaphorically, this guarantess that similar fragments 'repel' each other and are less likely to be part of the same draw. Mathematically, this means probabilities of random subsets of sounds are assinged according to the determinant of a function. In other words, a feature extraction function (see below a dimensionally-reduced UMAP picture of the features). In this way sets of vectorised audio fragments are drawn at random in a way that their features are maximally contrasting. As opposed to other generative systems, such as those based on latent diffusion, this experimental method of sampling advances a new form of archival listening and live improvisation. Not passively prompting with words, but live dubbing and remixing fragments ala musique concrète.

<div class="12u"><span class="image fit"><img src="{{ site.baseurl }}/images/dpp_sampling/hutchinson_UMAP.png" alt="" /></span></div>

# Event flyer and credits

<div class="12u"><span class="image fit"><img src="{{ site.baseurl }}/images/dpp_sampling/uts-eflyer.png" alt="" /></span></div>

Special thanks to Andrew Burrell and Zoë Sadokierski for including my proposal in the research event programme.
