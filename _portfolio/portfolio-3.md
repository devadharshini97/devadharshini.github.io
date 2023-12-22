---
title: "Attribute-Based Image Manipulation with Conditional Variational Autoencoder"
excerpt: "In this project, I implemented a Conditional Variational Autoencoder (CVAE) to encode and manipulate images from the CelebA dataset, comprising over 200,000 celebrity images with 40 face attributes. The CVAE, designed with specific preprocessing steps, encoder architecture, and decoder components, aimed to generate realistic reconstructions while considering attribute changes. Tasks included manipulating images based on attribute vectors and smoothly morphing between two images through linear interpolation in the latent space, showcasing the model's versatility in image generation and manipulation.<br/>"
---

In this project, I developed a Conditional Variational Autoencoder (CVAE) to encode and manipulate images from the CelebA dataset. The dataset comprises over 200,000 celebrity images, each annotated with 40 binary face attributes such as gender, smile, and glasses. My objective was to implement a CVAE capable of encoding these attributes and generating realistic image reconstructions.

The CVAE implementation involved several key steps:

Image Preprocessing: I resized images to [3, 64, 64] and normalized pixel values to the range [0, 1].

Attribute Channel Addition: I added a fourth channel to each image to encode attribute annotations. A fully-connected layer processed the 40-dimensional attribute vector, and the resulting matrix was concatenated as a fourth channel to the original image.

Encoder Architecture: I designed an encoder model with five Conv2D layers, each using [3, 3] shaped kernels, stride 2, padding 1, and Leaky ReLU activations. The number of kernels in these layers were (32, 64, 128, 256, and 512). The flattened outputs encoded the mean (µ) and standard deviation (Σ) parameters of the distribution of the latent variable (z).

Reparameterization Trick: I utilized the reparameterization trick to sample the latent variable (z).

Decoder Architecture: I implemented a decoder using five Transposed 2D Convolutional layers with [3, 3] shaped kernels, stride 2, padding 1, and Leaky ReLU activations. A final convolutional layer with Tanh activation reconstructed the original normalized image.

Reconstruction Loss: I applied Mean Squared Error as the reconstruction loss.

Task 2 involved using the trained CVAE to manipulate images by changing the attribute vector input. I encoded images from the test set, specified new attributes, and decoded the mean vectors combined with the new attributes using the pre-trained decoder. Examples of manipulations included converting non-smiling faces to smiling, non-mustached to mustached, and non-glass-wearing to glass-wearing.
![original_dataset](https://github.com/devadharshini97/devadharshini.github.io/assets/41442650/7da2bd2a-4e45-44a0-833b-40d15ea62977)

*Figure 1: Original Dataset*

![Manipulated_faces_with_glass](https://github.com/devadharshini97/devadharshini.github.io/assets/41442650/09a39f56-c721-4174-8d70-28f266824b58)

*Figure 2: Manipulated Faces with Glasses*

Task 3 focused on slowly morphing one image into another using linear interpolation in the latent space. By obtaining the mean vectors of two images, I linearly moved along the interpolation vector to generate new samples that represented a smooth transition between the original images.

![Image_morphing](https://github.com/devadharshini97/devadharshini.github.io/assets/41442650/8a37c5fe-5331-4e5b-afd3-a1e9aa9e57f1)

*Figure 3: Image Morphing*

The project showcased my proficiency in implementing a CVAE for image manipulation and demonstrated the model's ability to generate diverse and realistic image reconstructions based on attribute changes and linear interpolation in the latent space.
