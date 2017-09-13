---
title: Setup for deep learning
author: ''
date: '2017-09-06'
slug: setup-for-deep-learning
summary: Setting up a pc for deep learning and first show-off of some neural style transfer
tags:
  - Deep learning
  - Neural-style-transfer
header:
  image: headers\cgp-neural-style-transfer.jpg
---

## Setup for deep learning
  
Having recently started on Andrew Ngs new Deep Learning Specialization on Coursera. I have done some research on what would be a good setup to do deep learning/neural networks.  
For now it seems that having your own pc with a good graphics cards can be a better choice economically, than relying on cloud services. That was ringing bells for me, because i have thought for some time to upgrade the old dust-collector.  
So money has been invested in a new pc, with a 1080 ti Nvidia graphics card. Now setup with CUDA and cuDNN to take advantage of the gpu, especially on neural networks.  
Rstudios keras has been setup, with Anaconda to make python environments for some of the more popular deep learning frameworks like TensorFlow (googles framework) and CNTK (microsofts framework).  

Btw the setup has been far from plug and play. There is guidelines to install all the different tools, but usually there was always something that was abit off, so it had to be nudged in the right place before the installations would work, so quite some time has been used googling and looking through github-issues to find the fix that would work for my setup.  

## First steps in deep learning
  
Now with the computer set up and spinning, its time to get to work. The wonderfull thing about deep learning is that there is alot of open sources stuff to try, so its just to find something interesting, grab the code and see if you can get it to work.  

The thing i found interesting to show-off here, is whats called "neural style transfer" and i am using the implementation done by Anish Athalye found [here](https://github.com/anishathalye/neural-style)

The intuition with neural style transfer is that neural networks has been great to grasp what an image represents, it can analyze all the pixels, and collect exactly those combinations of pixels that shapes the contours of a face or an object or whatever it has been trained to find. It can be trained to find the content of the image.  
But a neural network can also be used to find the textures of an image, so instead of finding the contents its finding the style used. These 2 things can be done independently, so in one image you can take the content, and then from another image you take the style. When recombined something new is created with the basic structures from the first image, and the general style from the second image.  

Thats what can be seen in the header of this post. From left to right its my profile picture, first done with the style of Van Goghs Starry Night, then Pablo Picassos Guernica and lastly a picture of the milky way.  

 Van Gogh  |  Picasso  | the milky way
:---------:|:---------:|:--------------:
![](/img/nst/1-style.jpg "Starry Night") | ![](/img/nst/guernica.jpg "Guernica") | ![](/img/nst/milky-way.jpg "The milky way")

In the implementation from Anish there are lots of possibilites to adjust the parameters in how this is created, so alot of time can be spent experimenting with this. But for now its enough showing off with the visual stuff. Maybe next time it will be something more serious, like how i used deep learning to conquer the world.
