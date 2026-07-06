---
title: "VoxelAdv: Adversarial Semantic Attack Synthesis for 3D Data"
excerpt: "A Voxel-Based Adversarial Semantic Attack Synthetic Data Generation Pipeline"
collection: portfolio
---

You can find the github link here: https://github.com/ziHanDing579/voxelAdv

This is a computer vision class project that I thought was rather well done. At least for a first attempt at security intersect computer vision.

I had known about adversarial attacks in computer vision for quite a while now. In fact, at the first or second class of my computer visions course at Pitt, I had asked the professor about what other areas in computer vision intersects security, at the time, I thought security in computer vision was over. Adversarial attacks have been tackled with adversarial learning to gain adversarial robustness.

But turns out, other forms of adversarial attacks have been found. Such as prompt injections, and most importantly, semantic attacks. Attacks that exploits the lights and shadow. Physical conditions that can occur in nature, which is a much more relevant threat to application than regular adversarial attacks.

Just so happens I was playing Minecraft and when it was time to come up with a project, I wanted to tie Minecraft into this security computer vision hybrid thing. The project was born.

The whole idea is to provide a cheaper and more mangeable platform for synthesizing adversarial data for computer vision models. Traditional approaches either took too much time and manpower or too much compute. Minecraft acted as a nice platform where people can build or import 3D models of their product easily and mess with the physicals conditions as they pleased via shaderpacks.

As with all things in academia, when actually trying to get the pipeline setup, me and my teammate ran into several problems. The biggest of which was neither of us had experience with Minecraft shader language. For that, we relied on using a simple shaderpack and Claude Opus 4.7 to help deal with the shader to Python conversion. It wasn't great, but it did manage to get the very basics done. Then it was outdated academic software that we thought was available. Had to monkey patch my way through an older version to get it compatible with our setup. Fine-tuning models for Minecraft scene recognition also took significant time and compute and credits to Wafik for getting it done.

Now a voxelized world is certainly not a complete real world parallel but me and my teammate found something very interesting here. Even a light modification to the scene with some blur can cause a significant drop in scene recognition even with newer models like Gemma 4 or Qwen 3 by 20% or so. With our optuna adversarial setting generation, we managed to reduce the accuracy of both models to well below the random baseline.

You can find more details at our paper on: https://github.com/Wafik20/voxel-based-adversarial-attacks/blob/main/paper/voxel_based_adversarial_attacks.pdf 