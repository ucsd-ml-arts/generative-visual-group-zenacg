# Project 4 Generative Visual

Yunchieh Chang, cyunchie@ucsd.edu

## Abstract

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
  Following we have presented some of our results in the order of the number of the parameter EPOCH
  * EPOCH = 34   
  Things just get started. We can see in the image below that the network is able to generate some transform pairs, but the generated faces still look blurry.
    ![34_0](Images/34_2.jpg)
    ![34_1](Images/34_77000.jpg)
  * EPOCH = 75   
  As we can in the images below, the results highly dependent on the color and lighting of the images. For example, a black and white photo could be a match with a picture of a dog with white fur and black eyes, and there's a high chance that a woman with light brown, long hair would be transformed into a male lion. 
    ![75_0](Images/75_2.jpg)
    ![75_1](Images/75_1667055.jpg)
  * EPOCH = 76   
  Since the program is still learning, it's possible that it would generate some new species. For example, a dog-like creature with long long beard.
    ![76_0](Images/76_168100.jpg)
    ![76_1](Images/76_168650.jpg) 
  To match the shape of the faces, most of the results are able to keep the animals' lop or erect ears.
    ![76_2](Images/76_169550.jpg)
    ![76_3](Images/76_169650.jpg)      
  * EPOCH = 79   
  The program even tries to imitate a flirtatious facial expression althought the result looks angry.
    ![79](Images/77_79.jpg)         
  * EPOCH = 81   
  Before we have seen some results of transforming a male line to a woman. For now, the lion could keep the hair style, bang when transformed from a human.
    ![81](Images/81.jpg)     
  * EPOCH = 86  
  A polar bear's mounth turns out to be a man's beard.
    ![86](Images/86.jpg)        
  * EPOCH = 120  
  Seems that it's possible that a beagle and a woman share taste in clothes.
    ![120_266700](Images/120_266700.jpg)           
    ![120](Images/120.png)              
  * EPOCH = 122 
  Last but not the least, a chill male lion turns out to be a painting-like male human.
    ![122](Images/122.jpg)

## Technical Notes

Any implementation details or notes we need to repeat your work. 
- The program is iteratively trained with EPOCH = 120, and takes around 14 hours to run. 
- Images are resized into 128x128 due to the runtime limitation.

## Reference

References to any papers, techniques, repositories you used:
- Papers
  * [CycleGAN with Better Cycles](https://ssnl.github.io/better_cycles/report.pdf)

- Repositories
  * [pytorch-CycleGAN-and-pix2pix](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix)

- Blog posts
  * [Understanding and Implementing CycleGAN in TensorFlow](https://hardikbansal.github.io/CycleGANBlog/)
  * [Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks](https://junyanz.github.io/CycleGAN/)
