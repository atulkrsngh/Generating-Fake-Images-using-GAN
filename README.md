# Generating-Fake-Images-using-GAN
Generative Adversarial Neural Network to Generate Fake Images based on MNIST dataset

Training Phases  
Phase 1 - Train Discriminator  
Phase 2 - Train Generator     

Phase 1: Discriminator  
Real images (labeled 1) are combined with fake images from generator (labeled 0).  
Discriminator trains to distinguish real from fake (with backpropagation only on discriminator weights)  

Phase 2: Generator  
Produce fake images with generator.   
Feed only these fake images to the generator with all labels set as real (1).  
This causes the generator to attempt to produce images the discriminator believes to be real.  

Because we feed in fake images all with labeled 1, we only perform backpropagation on the generator weights in this step.  

The generator never gets to see the actual real images!  
It generates convincing images only based off gradients flowing back through the discriminator.  


