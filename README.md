# Project 4 Generative Visual

Yunchieh Chang, cyunchie@ucsd.edu

## Abstract

Include your abstract here. This should be one paragraph clearly describing your concept, method, and results. This should tell us what architecture/approach you used. Also describe your creative goals, and whether you were successful in achieving them. Also could describe future directions.

In this project, we use a CycleGAN to learn to translate an image from a source domain, a face matching data set to a target domain, the animal faces data set in the absence of paired examples. It contains a generator network and a discriminator network beating each other while the generator takes a picture from the face matching data set tries to generate a realistic animal face image to trick the discriminator. Similarly, there's also another generator generate images in reverse direction to beat with the discriminator, which completes the so-called "Cycle"GAN.

Since the animal faces data set contains wide diversity of animal species, some of the results barely make sense and look vaguely. Therefore, an experiment of training a network to translate human faces to a certain kind of species, say, cat, is a future work direction. More details about our work is discussed in Section "Results".

## Model/Data

Briefly describe the files that are included with your repository:
- training data (or link to training data)
  * [Face matching data set](https://cyberextruder.com/face-matching-data-set-download/)
    * The data set contains 10,205 images of 1000 people scraped from the internet. 
    * All images have size 600 x 600 pixels and are stored with jpeg compression.

  * [Animal faces data set](http://www.stat.ucla.edu/~zzsi/HiT/exp5.html)
    * The data set contains 2461 images of 20 different species of animals. 

  * [Cat data set](https://www.kaggle.com/crawford/cat-dataset/downloads/cat-dataset.zip/2)
    * The data set contains over 9,000 cat images.

## Code

Your code for generating your project:
- Jupyter notebooks: humanToAnimal.ipynb

## Results

Documentation of your results in an appropriate format, both links to files and a brief description of their contents:
- image files (`.jpg`, `.png` or whatever else is appropriate)
  * Following we have presented some of our results in the order of the number of the parameter EPOCH
   * EPOCH = 34
     ![34_0](Images/34_2.jpg)
     ![34_1](Images/34_77000.jpg)
   * EPOCH = 75
     ![75_0](Images/75_2.jpg)
     ![75_1](Images/75_1667055.jpg)
   * EPOCH = 76   
     ![76_0](Images/76_168100.jpg)
     ![76_1](Images/76_168650.jpg) 
     ![76_2](Images/76_169550.jpg)
     ![76_3](Images/76_169650.jpg)      
   * EPOCH = 79
     ![79](Images/77_79.jpg)         
   * EPOCH = 81
     ![81](Images/81.jpg)     
   * EPOCH = 86
     ![86](Images/86.jpg)        
   * EPOCH = 120
     ![120_266700](Images/120_266700.jpg)           
     ![120](Images/120.jpg)              
   * EPOCH = 122
     ![122](Images/122.jpg)
   * EPOCH = 123
     ![123](Images/123.jpg)   

## Technical Notes

Any implementation details or notes we need to repeat your work. 
- Does this code require other pip packages, software, etc?
- Does it run on some other (non-datahub) platform? (CoLab, etc.)

## Reference

References to any papers, techniques, repositories you used:
- Papers
  * [CycleGAN with Better Cycles](https://ssnl.github.io/better_cycles/report.pdf)

- Repositories
  * [pytorch-CycleGAN-and-pix2pix](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix)

- Blog posts
  * [Understanding and Implementing CycleGAN in TensorFlow](https://hardikbansal.github.io/CycleGANBlog/)
  * [Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks](https://junyanz.github.io/CycleGAN/)
