---
title: "Exploring the GLIDE model for Human Action-effect Prediction"
collection: Proceedings of the workshop on People in Vision, Language, and the Mind @LREC2022
permalink: /publication/2022-PVLAM
excerpt: 'Diffusion Model, Image Manipulation'
date: 2022-06-20
venue: 'P-VLAM'
paperurl: 'https://aclanthology.org/2022.pvlam-1.pdf#page=9'
citation: '<span style="color: red;">Fangjun Li</span>, et al. Exploring the GLIDE model for Human Action-effect Prediction. P-VLAM (2022): 1.'
---

We address the following action-effect prediction task. Given an image depicting an initial state of the world and an action expressed in text, predict an image depicting the state of the world following the action. The prediction should have the same scene context as the input image. We explore the use of the recently proposed GLIDE model for performing this task. GLIDE is a generative neural network that can synthesize (inpaint) masked areas of an image, conditioned on a short piece of text. Our idea is to mask-out a region of the input image where the effect of the action is expected to occur. GLIDE is then used to inpaint the masked region conditioned on the required action. In this way, the resulting image has the same background context as the input image, updated to show the effect of the action. We give qualitative results from experiments using the EPIC dataset of ego-centric videos labelled with actions.


![test](/images/PVLAM-01.png)
![test](/images/PVLAM-02.png)
![test](/images/PVLAM-03.png)
![test](/images/PVLAM-04.png)