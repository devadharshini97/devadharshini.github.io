---
title: "Normalizing FLow Architecture"
excerpt: "In this project, I designed a Normalizing Flow architecture using Neural Radiance Fields to transform 2D points into a standard normal distribution. The architecture includes affine coupling layers with neural network-modeled scaling and translation functions. I trained separate models for different datasets, evaluating their performance through scatter plots, loss analysis, and exploring the impact of hyperparameter choices.<br/>"
---

"In this project, I worked with two datasets, each divided into training and test sets, comprising 2D points following specific distributions. The goal was to design a Normalizing Flow architecture, with transformations f : x -> z and (f)^{-1} : z -> x, aiming to transform points x into z ~ N(0, I<sub>2</sub>), where 0 = [0, 0]^T and I<sub>2</sub> is the 2 × 2 identity matrix. The architecture involved a series of affine coupling layers (f = f<sub>1</sub> o f<sub>2</sub> o ... o f<sub>k</sub>), each with scaling and translation functions modeled using neural networks.

Key Architecture Details:
1. Implemented f as a composition of affine coupling layers.
2. Modeled scaling and translation functions using neural networks with one hidden layer each.
3. Incorporated reversal or permutation operations between affine coupling transformations.
4. Tunable hyperparameters included the number of layers and neurons in hidden layers.
5. Defined the model as a callable class for flexibility in training and testing.

Training Details:
1. Trained separate models for each dataset and hyperparameter choice.
2. Specifically trained one-, three-, and five-layered models for each dataset.
3. Evaluated the distribution of z using the trained model and test dataset.
4. Generated new points \(\hat{x}\) by sampling \(z\) from \(N(0, I_2)\).
5. Showed combined scatter plots of \(x\) from the test set and \(\hat{x}\) to illustrate distribution matching.
6. Plotted epoch-wise loss for each model.

Deliverables:
1. Submitted loss plots and scatter plots for each model.
2. Discussed the expected appearance of the scatter plot of \(z\) and observed variations based on hyperparameters.
3. Analyzed how distribution matching between \(\hat{x}\) and \(x\) changed with the number of layers.
4. Explored the ease of training for each dataset and speculated on reasons.
5. Demonstrated the impact of changing hidden layer size using one dataset."





