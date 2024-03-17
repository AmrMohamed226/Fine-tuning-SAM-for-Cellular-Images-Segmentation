# Fine-tuning Segment Anything Model (SAM) on Electron Microscopic Cellular Images for Mitochondrial Segmentation

## Overview
This project aims to fine-tune Meta AI's Segment Anything Model (SAM) for the specific task of segmenting mitochondria in electron microscopic images of cells. Leveraging the state-of-the-art capabilities of SAM, the project focuses on adapting the model to excel in identifying and outlining mitochondria within the complex structures observed in cellular level images. The EPFL Electron Microscopy Dataset serves as the training ground, with its detailed images and segmentation masks of mitochondria, to refine SAM's segmentation prowess in this specialized domain.

## Techniques and Components
### 1. Dataset Utilization
- Adopts the EPFL Electron Microscopy Dataset featuring detailed cellular images with segmentation masks of mitochondria.
- Implements image patching techniques to enhance the model's focus on relevant cellular structures, optimizing for detailed segmentation.

### 2. SAM Model Adaptation
- Focuses fine-tuning efforts on the mask decoder of SAM to refine its segmentation capabilities specifically for mitochondrial structures.
- Maintains the integrity of the image and prompt encoders by freezing their weights to preserve the model's broad segmentation abilities.

### 3. Custom Loss Function
- Employs a combination of Dice loss and Cross-Entropy Loss to balance pixel-wise classification accuracy with boundary delineation precision.
- Optimizes model learning using the Adam optimizer with carefully chosen parameters to facilitate effective fine-tuning.

### 4. Evaluation Metrics
- Utilizes Sørensen–Dice coefficient and Intersection over Union (IoU) score to quantify model performance, focusing on the overlap and accuracy of predicted segmentation masks against ground truth.

### 5. Model Training and Evaluation
- Conducts rigorous training and evaluation phases to compare the fine-tuned SAM model against its base version, demonstrating significant improvements in mitochondrial segmentation.

## Performance Insights
### 1. Enhanced Segmentation Accuracy
- Demonstrates a substantial increase in both Dice score and IoU score post-fine-tuning, indicating improved segmentation precision and overlap with ground truth masks.

### 2. Visual Validation
- Provides comparative visual evidence of the fine-tuned model's superior segmentation capability over the base SAM model, especially in complex images with multiple mitochondria.

![SAM results](./Images/SAM%20results.png)

## Challenges and Future Directions
- Acknowledges computational resource limitations as a primary constraint, suggesting future explorations into alternative architectures and optimization strategies.
- Proposes further investigation into model's adaptability and performance across varying datasets and segmentation tasks beyond mitochondrial structures.
