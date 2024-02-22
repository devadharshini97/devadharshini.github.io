---
title: "Deepfake Detection Model "
excerpt: "Implemented two approaches, utilizing Xceptionet and metric learning, to achieve higher accuracy in classifying low-resolution videos. Developed a model employing MTCNNs to distinguish between authentic and manipulated videos, achieving an initial accuracy of 92%. Further enhanced accuracy by 10% on low-resolution videos through the integration of metric learning techniques.<br/>"
---

In response to the escalating threat of deepfake technology and its potential misuse in disinformation and propaganda, our project focuses on developing robust methods for deepfake detection. Leveraging Multitask Cascaded CNNs (MTCNN), FaceNet, and metric learning, we devised a comprehensive approach to discern authentic from manipulated videos. Our work explores deep learning strategies in the context of deepfake classification, particularly in high compression scenarios, demonstrating the effectiveness of metric learning in this challenging task.

By utilizing fewer frames per video to assess realism, our metric learning approach, employing a triplet network architecture, proves fruitful. This innovative technique enhances the feature space distance between clusters of real and fake video embedding vectors. Validation on Celeb-DF and Celeb-DF-v2 datasets, which include interviews of 52 celebrities on YouTube, showcased the adaptability of our methods across diverse environments.

The training process involved approximately 30,000 images with equal distribution between manipulated and original images, and categorical labels denoting real or manipulated. Employing semi-hard triplet loss, our model considered 25 frames per video, generating 512 face embedding vectors using FaceNet. The network trained with triplet loss served as input for classifiers such as KNN, SGD, and Random Forest, achieving high accuracy in real vs. fake face classification.

Comparing architectures, we found that our model, consisting of MTCNN followed by FaceNet with triplet loss and two classifiers (SGD and Random Forest), outperformed the XceptionNet. We successfully addressed the challenges of spatio-temporal learning and low accuracy associated with convolution-based networks like XceptionNet.

Our model's ability to accurately classify real and fake faces was evident in achieving a testing accuracy of 87%. During testing, video frames were processed, predictions made on features extracted from 25 frames, and the mean used for final classification output. In summary, our innovative approach, combining MTCNN, FaceNet, and metric learning, offers a powerful solution for the detection of deepfake videos, showcasing superior accuracy and resilience against various challenges.

![deep_fake](https://github.com/devadharshini97/devadharshini.github.io/assets/41442650/4956ac25-f7d9-4a1b-810c-a3faf67ac7c5)
