# AI-Art

***

## Motivation

Creativity is something we closely associate with what it means to be human. But with digital technology now enabling machines to recognize, learn from and respond to humans and the world, an inevitable question follows: 

> Can machine be creative? And will artificial intelligence ever be able to make art?

Recent art experiments are the use of "generative adversarial networks" (GANs). GANs are "neural networks" that teach themselves through their own experimentation, rather than being programmed by humans. *It could be argued that the ability of machines to learn what things look like, and then make convincing new examples, marks the advent of "creative" AI.*

I will cover three different methods by which you can create novel arts, solely by code - **Neural Style Transfer, CycleGAN,** and **Pix2pix.**  

***

## Neural Style Transfer

Neural Style Transfer (NST) is one of the most fun techniques in deep learning. As seen below, it merges two images, namely, a "content" image (C) and a "style" image (S), to create a "generated" image (G). The generated image G combines the "content" of the image C with the "style" of image S. 

![neural-style](https://user-images.githubusercontent.com/41862477/49682529-b23e2880-fadb-11e8-8625-82fc2b14c487.png)

Neural Style Transfer (NST) uses a previously trained convolutional network, and builds on top of that. I will use VGG-19 which has already been trained on the very large ImageNet database. It learned to recognize a variety of *low level features* (at the earlier layers) and *high level features* (at the deeper layers). Building the NST algorithm takes three steps:

**Content Cost**:  ```Jcontent (C, G)```
**Style Cost**  :  ```Jstyle (S, G)``` 
**TV Cost**     :  ```Jtv (G) ```

*Putting all together*  :  J(G) = (alpha) * Jcontent (C, G) + (beta) * Jstyle (S, G) + (gamma)* Jtv (G).

### 
