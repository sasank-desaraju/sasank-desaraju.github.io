---
layout: single
title:  "Medical Students And Chatbots"
header:
  teaser: "torii.jpg"
categories: 
  - Medicine
  - Machine Learning
tags:
  - medicine
  - machine learning
---

Hello, World!


This is about the similarities between the medical student learning process and LLM training process.

Pretraining = Anki

RLHF = Clinical Practice such as EAC


If med students are great at Anki, do they really *know* the information?
- Mention memorizing Anki card clozes. This is analogous to overfitting.
- There are even instagram memes about students failing to recognize the semantic content of "currant jelly sputum" (K. pneumoniae) in the clinic.


Humans are good at navigating the sparse rewards of clinical practice, but LLMs are not so good at navigating the sparse rewards of RLHF.


Maybe UWorld and other practice questions are reinforcement learning with verifiable rewards.
Mid-training: UWorld questions, maybe


Supervised FT and writing notes



Studying in medical school while training deep learning models on a supercomputer, I have had front row seats to both medical training and AI training.
On the surface, these may seem quite different, but over time I found some parallels between the processes that produce doctors and ChatGPT.
I hope this blog post can show these similarities to you, dear reader, and maybe help bridge some knowledge from one domain to the other.

> Note: I will focus on autoregressive large language models (e.g. ChatGPT), even though many other AI models exist.

# Overview:
- A note on stages
    - LLM training used to have a straight order, and also many stages didn't exist. Now there's more mixing. Lot of mixing already in medical training.
- Pre-training and Anki
    - Spaced Repition and Data Sampling
    - High Yield Cards and Data Quality (maybe leave this out)
- Mid-training/RLVR and UWorld
    - Low Yield Goblins
    - Currant jelly sputum (buzzword fixation + loss of semantic understanding)
- SFT and Clinical Rotations (Copycat)
- RLHF and Clinical Rotations (Feedback)
- Self-supervised/continual learning and medical practice



# A note on stages

I've organized this by the different discrete "stages" of training, which are not as distinct in practice as I've laid out here.
The precursor to the original ChatGPT was called GPT-3 and had only the pre-training stage, meaning it only completed sentences and couldn't hold a conversation.
ChatGPT's SFT and RLHF (more later) enabled nice conversation.
Nowadays, the "recipe" of training an LLM is a whole field of its own, with models following the general path I've laid out but popping back or forward a step based on the educated guesses and small-scale experiments of the technical staff.
Medical training has a lot of mixing (like most human learning).
A first year medical student may take a break from their Anki (pre-training) to volunteer in a clinic led by their seniors (SFT and RLHF).
Medical schools, in fact, advertise these "early clinical experiences" to prospective applicants.
Basically, I don't want to give you the false idea that these stages are a rigid, one-way progression in either discipline.



# 1. Pre-training and Anki

The first step to training an LLM involves "eating the internet".
You download all of Wikipedia, Reddit, Twitter, and anything else you can get your hands on.
You spin up your fresh, randomized AI model and feed it the first few words of a sentence: "The capital of France is".
Then you ask it to guess what comes next.
A little detail is that you split your vocabulary of words into few-letter bits called "tokens" and you guess those.
If the model guesses the token "Ber", then you adjust the model parameters (loss function + gradient descent) in the direction of "Par".
You then do this for entire Wikipedia articles and so forth.

> Behold! Next Token Prediction!

This is actually pretty powerful when done at scale.
One of the most famous datasets for this, [The Pile](https://pile.eleuther.ai/), was released in 2020 at over 800 GB and pales in comparison to what the big AI labs are using these days.

Medical students do something similar for the first two years of school.
We use a computer flashcard app called [Anki](https://apps.ankiweb.net/), where the cards have a front side with a fill-in-the-blank sentence and a back with the full sentence and related helpful information.
We spend hours each day reading the front, guessing the blank, and flipping the card to how we did.
This helps us learn factual information such as drug names and indications, anatomy (the blanks are on cadaveric pictures), disease symptoms, and so on.

The scale is what makes it a challenge.
The popular AnKing deck that covers USMLE Step 1 board exam material numbers 25,000 **check this** cards.
Some of my classmates regularly did 2,000 cards a day.
(I only broke 1k a few times.)






## Spaced Reptition and Data Sampling
## Overfitting
## But what are lectures? (maybe pre-training, maybe SFT, idk maybe something else)
# 2. Mid-training/RLVR and UWorld
## Low Yield Goblins
## Currant jelly sputum (buzzword fixation + loss of semantic understanding)
# 3. SFT and Clinical Rotations (Copycat)
# 4. RLHF and Clinical Rotations (Feedback)

Hidden curriculum shows conflict between SFT and RLHF: not following guidelines and huffing at the frequent flyer

# 5+. Self-supervised/continual learning and medical practice



