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

## Key Findings
- Data augmentation improved model robustness and reduced overfitting.
- RMSprop outperformed both Adam and SGD.
- The pre-trained MobileNetV2 model achieved higher accuracy than the custom CNN, but struggled with real-world images due to domain mismatch.
- Fine-tuning MobileNetV2 improved performance on real-world data, but findings suggest that additional diverse training data is necessary for true generalization.

## Future Work
- Collect and train on more diverse, noisy datasets.
- Explore ensemble learning methods to improve generalization performance.
