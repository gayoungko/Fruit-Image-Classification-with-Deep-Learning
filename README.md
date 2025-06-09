# Fruit-Image-Classification-with-Deep-Learning

# Fruit Image Classification with CNN and MobileNetV2

**Authors:** Gayoung (Ellena) Ko, Sijia (Neveah) Zhan  

This project classifies fruit images using a custom CNN and transfer learning with MobileNetV2. We compare data augmentation strategies and optimizers, and evaluate model generalization using real-world images we collected ourselves.

## Dataset
We used the [Fruits-360 dataset](https://www.kaggle.com/datasets/moltean/fruits) from Kaggle.

## Key Findings
- Data augmentation increased model robustness and reduced overfitting.
- RMSprop outperformed both Adam and SGD. 
- The pre-trained MobileNetV2 model achieved higher accuracy than the custom CNN, but struggled with real-world images due to domain mismatch.
- Fine-tuning MobileNetV2 improved performance on real-world images, but the results suggest that training on more diverse, real-world data is essential for true generalization.


## Future Work
- Collect more diverse, noisy data.
- Explore ensemble learning for better generalization.
