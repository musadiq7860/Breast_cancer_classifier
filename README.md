________________________________________
# Breast Cancer Detection Using CNN and Transfer Learning
# Dataset and Preprocessing
A subset of the Breast Cancer Histopathological Dataset (1,000 images) was used for this experiment. Images were resized to 128×128 pixels and normalized to pixel values between 0 and 1. The dataset was split into training and validation sets (80:20 ratio). The validation set contained 200 images.
Model 1: Custom CNN
A simple CNN with three convolutional layers followed by max pooling, flattening, and dense layers was trained for 10 epochs.
•	Training Accuracy: ~62%
•	Validation Accuracy: ~55%
•	Observation: The model learned some features but struggled to generalize well to unseen validation images. Limited dataset size and complexity reduced performance.
# Model 2: Transfer Learning with VGG16
A pre-trained VGG16 model (with ImageNet weights) was used as a feature extractor. A flatten layer, dense ReLU layer, and dropout were added, followed by a sigmoid output layer. The base model was frozen, and the network was trained for 10 epochs.
•	Training Accuracy: ~65%
•	Validation Accuracy: ~53–58%
•	Observation: Transfer learning provided slightly better results than the custom CNN. However, due to the small dataset, the model still showed overfitting (high training accuracy vs. lower validation accuracy).
# Evaluation
Both models showed moderate performance but were limited by the dataset size. Validation accuracy remained in the 50–58% range, indicating that the models could not reliably detect cancer in unseen images. Increasing dataset size, using stronger augmentation, or fine-tuning VGG16 could improve results.
# Conclusion
The experiment demonstrates the challenges of using deep learning with small datasets. While a basic CNN provided a foundation, transfer learning with VGG16 improved feature extraction and accuracy. Future work should involve larger datasets and fine-tuning to achieve clinically relevant performance.
________________________________________



