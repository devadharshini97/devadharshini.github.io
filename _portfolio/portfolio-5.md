---
title: "Laplacian Blob Detection"
excerpt: "This image processing project employs a Laplacian of Gaussian filter to detect distinct regions (blobs) in images, revealing valuable information undetected by conventional methods. The algorithm efficiently highlights and displays these blobs on the input image, demonstrating its effectiveness in object recognition and tracking.<br/>"
---

The Blob Detection project focuses on identifying regions within an image that exhibit variations in properties like color or brightness compared to their surroundings. These distinct regions, termed "blobs," provide complementary information that may go undetected by traditional edge or corner detectors. The project's applications include object recognition, object tracking, and peak detection in segmentation scenarios.

## Algorithm:
The algorithm comprises four key steps:

## 1. Creation of Laplacian of Gaussian filter:

Utilizes the Laplacian of Gaussian (LoG) filter to highlight rapid intensity changes.
Mathematically represented as the convolution of the Laplacian and Gaussian filters.
Implemented using the fspecial() function with a user-defined sigma value (1.3 in this case) to balance runtime and detection accuracy.

## 2. Building a Laplacian Scale Space and Convolution:

Constructs a Laplacian scale space by incrementing the scale space size and resizing the input image.
Convolution with the LoG filter and squaring the result.
Stores the processed images in a 3D matrix, space_scale, during each iteration.

## 3. Performing Non-Max Suppression in Scale Space:

Implements Non-Max Suppression based on Harris's method with a threshold value of 1000.
Eliminates redundancy by storing coordinates of maxima in a separate cell matrix.
Applies non-max suppression to prevent repeated coordinates, excluding edge detections.

## 4. Displaying Resulting Circles at Characteristic Scales:

Plots circles on the input image using the viscircles function.
Utilizes saved maxima coordinates and blob radii to showcase Blob Detection effectively.

### Implementation Highlights:

The LoG filter is created using the fspecial() function with careful consideration of filter size and standard deviation.
Experimentation led to selecting a sigma value of 1.3, balancing runtime efficiency and accurate blob detection.
Non-Max Suppression is fine-tuned with a threshold value of 1000, based on trials and compatibility with input images.
Circles are displayed on the input image using viscircles, visually demonstrating the success of Blob Detection.
This project not only showcases proficiency in image processing techniques but also highlights the ability to optimize parameters for efficient and accurate results in blob detection applications.
![blob_detection_1](https://github.com/devadharshini97/devadharshini.github.io/assets/41442650/92ea4fd0-1673-4191-ab29-7243872023f2)
![blob_detection_2](https://github.com/devadharshini97/devadharshini.github.io/assets/41442650/e6cdea9f-427a-4817-876e-2c3c9f97ee33)



