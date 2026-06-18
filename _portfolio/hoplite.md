---
title: "Hoplite: P2P Network"
excerpt: "A GRPC-based Peer-to-Peer network project using pseudorandom code as the encryption"
collection: portfolio
---

This is a course project using GRPC to create a simple P2P network communication with what I would call a cascading message system.

The core premise is fairly simple, you have nodes in a network, these nodes represent individual users. The node have some value of trust/friendship/metric, that based on their actions, increases or decreases. When the node does something positive, their values increase, the message spreads wider. Otherwise, message doesn't spread as much.

My part in this project was the encryption and local node discovery. During the semester I took this course, I also took a course at CMU for cryptography, which is why pseudorandom code (PRC) is involved in this small course project. The idea of PRC was just interesting at the time. How can you have an encryption system that is both pseudorandom enough that people can't tell it is encrypted, but also structured enough that people can encrypt and decrypt while suffering from errors. I highly recommend reading the original paper from Christ and Gunn 2024.

The original paper has a lot of maths in it, but essentially relied on Low Density Parity Code (LDPC), Learning Parity with Noise (LPN) and errors from the communication channel cancelling out with each other. It was intended to be used as a watermark system for large language models (LLMs), but it is still an asymmetric encryption, which makes it applicable for a P2P network like Hoplite.

Now we have a more scientific rationale for why we wanted to use PRC as an encryption method, all about how traffic for hoplite should be indistinguishable from regular communication etc, but in reality, it was more that I wanted to do something with this new interesting thing and Hoplite just came up.

How did it turn out? It works, all three properties of PRC not only works in theory but also in practice. However, the amount of actual bits needed to encrypt a message is too large that there is a huge traffic with each message, defeating the point of it being indistinguishable from regular traffic.

But the ends isn't really the point for me in this project. It was the journey. This was the first time that I tried to bring something pure theory into practice and the first challenge was to determine what reasonable values are for alpha, gamma, etc. Potentially there's better ways about this, but I chose trial and error and slowly tuned each parameter so that I ended up getting actually expected behavior from the scheme. The actual programming of the encryption scheme was fairly simple, bar the fact that I couldn't find a kernel function and had to code my own. The second challenge was then integrating the PRC into the GRPC system. I actually ended up redesigning the handshake protocol to fit PRC into the picture. (Not something I would do IRL but for a course project to do something interesting, this was necessary) 

Once the two challenges have been overcame, the rest was fairly simple. If I were to do this again, I would say potentially use an automated framework like how hyperparameter optimization works for ML to find the correct values as opposed to my trial and error method. The other thing would be to focus on handshake design early as oppose to making quite a mess of it in the later stages of the project.

Very fun project, would do it again.