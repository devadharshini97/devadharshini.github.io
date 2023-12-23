---
title: "Single View Metrology Implementation"
excerpt: "Implementing the ICCV99 paper, this project extracts 3D geometry from a single perspective image through annotated line analysis, vanishing point computation, projection matrix derivation, and generation of texture maps for immersive 3D model visualization.<br/>"
---

## Project Overview:
This project involves the implementation of the "Single View Metrology" paper by Criminisi, Reid, and Zisserman (ICCV99). The objective is to compute aspects of the affine 3D geometry of a scene from a single perspective image with prior knowledge. The implementation encompasses four main tasks:

### Image Acquisition:

Captured a 3-point perspective image as input, following the guidelines of three-point perspective.
The input image is annotated to identify box vertices, essential for subsequent calculations.

### Computing Vanishing Points:

Annotated image lines are utilized to compute vanishing points using vector cross products.
Three vanishing points (Vx, Vy, Vz) are obtained with respect to the x, y, and z-coordinate systems.

### Projection Matrix and Homograph Matrix Computation:

The projection matrix is calculated using vanishing points, with scaling factors determined from reference coordinates.
Homograph matrices (Hxy, Hyz, Hxz) are derived from the projection matrix for XY, YZ, and ZX planes.

### Texture Maps and 3D Model Visualization:

Texture maps for XY, YZ, and XZ planes are created using reverse warping based on homograph matrices.
The project culminates in visualizing a reconstructed 3D model using Blender.

## Result:
The successful implementation of the "Single View Metrology" paper demonstrates the ability to extract meaningful 3D geometry from a single perspective image, with a clear focus on accuracy and robustness in annotation, computation, and visualization.



