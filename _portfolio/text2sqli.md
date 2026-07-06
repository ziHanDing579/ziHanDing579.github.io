---
title: "DaMiTSQL + MS Thesis Experiments"
excerpt: "Experiments for the DaMiTSQL Paper and the MS Thesis"
collection: portfolio
---

You can find the link to this project here: 

https://github.com/ziHanDing579/Text2SQLi

Since the publication of my DaMiT-SQL paper, I've worked on the code to create new models for my master's thesis. However, as not all of my experiments were successful and discussed in my thesis, I felt that an additional portfolio item is needed.

In my master's thesis, I largely used the given PCA + UMAP for my dimension reduction section, however, I actually started with dimension reduction as my main piece of research instead of the linear probe.

The initial setup was similar. I came up with the taxonomy. Wanted to see how these groups looked on a chart. At the time, whether it is due to poor hardware or poor procedure and code, I did not have a good visualization of the embedding clusters. So, I took it upon myself to improve that. Creating my own clustering layer on top of the sentenceBERT encoder to see if I can do better than the poor PCA + UMAP results. I tried a wide range of loss functions and created several hybrids that took into account the angle and the distance, getting better and better results as I went on. Eventually though, as I neared the deadline for my defense, I had to reproduce my earlier poor PCA + UMAP findings to show that this dimension reduction was necessary. This was after sending out the abstract and a month before the defense. 

Unfortunately or rather fortunately, I did not keep my PCA + UMAP code, so I had to write the code from scratch again. Turns out, PCA + UMAP does work and that my dimension reduction model was all for naught as it was worse than PCA + unsupervised UMAP and even worse than that, PCA + supervised UMAP had exactly what I wanted. Had to pivot, change the abstract and immediately proceed with additional experiments.

Regardless, I think this code is a nice exhibit of the attempts I made. Specifically, you will find the data, the generator for the malicious prompts and the machine learning attempts made in the repo.