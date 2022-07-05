# GAN-Models
Introduction
This Repository contains some PyTorch implementations of generative models, currently i have made implementations of Basic Convolutional AutoEncoder and Variational AutoEncoder.

Anime Faces Dataset
I have obtained the Dataset from this Repository animeGAN specifically this link which is made available by the owner of the aforementioned Repository.

Results
Convolutional AutoEncoder
Trained using MSE as Reconstruction Loss. I have trained on a subset of the dataset, due to a lot of variation in the dataset.

edit: the current notebook contains a mixture of BCE and MSE loss.

alt text

Variational AutoEncoder
I have tried training the VAE with a mixture of settings, NOTE: the amount of tests i have carried out are not exhaustive and i have trained the network to gain more insight into the VAE.

Trained using MSE loss as Reconstruction loss and KLDivergence loss as latent Loss

with beta=0.7 to sway model towards reconstruction.

on Unseen samples Unseen Dataset

on trained sample seen dataset

Trained using BCE loss as Reconstruction loss with beta=3 to have model generalize better

on Unseen samples Unseen Dataset

on trained sample seen dataset

Inference
Z must be increased(variable nz in vae network architecture) according to the image and is a best to be around the image dimension range.

Binary cross entropy turned out to be a slightly better reconstruction value as compared to MSE loss.

Weighing Beta of KLDivergence helps in managing between reconstruction vs generalization

As you can see in the above images, when you compare the output of the test images it is clear that the images generated with Beta as 3 is better at generalizing and creating better representations of the image.

Things To Do
GAN
References
I have mostly referred to Pytorch Examples for VAE

and this Repository for Conv-Autoencoder
