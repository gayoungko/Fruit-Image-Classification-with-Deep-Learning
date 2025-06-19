# Fruit-Image-Classification-with-Deep-Learning

**Authors:** Gayoung (Ellena) Ko, Sijia (Neveah) Zhan  

This project classifies fruit images using a custom CNN and transfer learning with MobileNetV2. We compare data augmentation strategies and optimizers, and evaluate model generalization using real-world images we collected ourselves.

## Dataset
We used the [Fruits-360 dataset](https://www.kaggle.com/datasets/moltean/fruits) from Kaggle.

## Files Included
1. `ds340_project (1).ipynb`:  
   Jupyter Notebook containing the complete code for model training, evaluation, and results.

2. `ds340_project_essay1`:  
   A written report detailing the methodology, experimental design, results, and conclusions of the project.

3. `By Gayoung (Ellena) Ko, (3).pdf` :
   Final presentation slides of the project.

## Methods

Focused on evaluating the real-world performance of deep learning models beyond clean datasets by building and testing fruit classification systems on images we collected ourselves.

1. Dataset Collection & Preprocessing
- Collected fruit images from grocery stores to build a custom real-world dataset with diverse lighting, backgrounds, and noise.
- Applied image preprocessing steps including resizing, normalization, and data augmentation (flip, zoom, translation).
- Organized the dataset using an 80/20 per-class stratified split to maintain class balance.

2. Model Development
- Built and trained a new CNN model and trained it with RMSprop optimizer.
- Implemented MobileNetV2 using pre-trained ImageNet weights.

3. Transfer Learning & Fine-Tuning
- Replaced MobileNetV2’s classifier with a new Dense softmax layer designed for our 8 custom fruit classes.
- Fine-tuned the entire MobileNetV2 model to adapt it to the real-world dataset, using a small learning rate for stability.

4. Evaluation
- Compared MobileNetV2's performance against our CNN on both the original Fruits-360 test set and our custom grocery store dataset.
- Evaluated generalization by analyzing classification accuracy and observing model behavior on noisy, real-world inputs.

## Challenges
The project began with a custom-built Convolutional Neural Network (CNN) trained on the Fruits-360 dataset (100×100 resolution). We experimented with various optimizers (Adam, RMSprop, SGD) and applied data augmentation techniques to improve generalization. However, challenges emerged:

1. The model performed poorly on the 100 x 100 dataset due to overfitting.
2. Even with augmentation, our CNN struggled with background variation, lighting differences, and natural noise present in real-world conditions.
3. We retrained a CNN and MobileNetV2 using the original-size Fruits-360 dataset, which included more realistic variation in image size and background. The model's performance on the test set improved significantly; however, it did not perform well on our own self-collected dataset again.

As a result, we shifted our approach:
We trained on an even messier, self-collected dataset. This allowed us to evaluate generalization more realistically and build a model that better reflected performance in everyday settings.

## Impact 
The work encourages future projects to incorporate more diverse and messy training data, as well as rigorous testing on custom-collected images, to improve model reliability in practical applications.
