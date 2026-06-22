# Classification of medical images: detection of pneumonia on X-ray images
This project was created as part of the Machine Learning course at the Computer Science graduate program.
# Main goal:
This project focuses on the classification of chest X-rays for the detection of pneumonia. The goal was to compare the performance of the adapted VGG16 architecture (transfer learning) with a simple baseline convolutional model, with special emphasis on the interpretability of the model using Grad-CAM visualization.
# Key features:
- ARCHITECTURE: Implementation and comparison of VGG16 (pre-trained) and custom baseline CNN.
- INTERPRETABILITY: Using the Grad-CAM algorithm to visualize regions in the image that most influenced the model's decision (Explainable AI).
- DATA PREPROCESSING: Using the CLAHE method to improve the contrast of medical images (in the application).
- GUI: Developed interactive application using the Streamlit library for easy model testing on new images.

# Results and metrics:
The models were evaluated on a test set of 624 images. Special emphasis is placed on responsiveness and specificity due to the nature of medical diagnostics (minimizing false negative results).
--- TEST set results for: Scratch CNN ---

Accuracy:    0.7468

Precision:   0.7125

Recall:      0.9974

F1 Score:    0.8312

Specificity: 0.3291


--- Results of the TEST set for: VGG16 ---

Accuracy:    0.8670

Precision:   0.8344

Recall:      0.9821

F1 Score:    0.9022

Specificity: 0.6752

!Note: Although the baseline has a high recall, the low specificity indicates that the model often classifies healthy patients as sick.

# Technologies used:
- Python
- PyTorch
- OpenCV, PIL
- Matplotlib, Seaborn
- Streamlit, Hugging Face

# Visualization (Grad-CAM):
The project includes the analysis of "black box" problems with neural networks. Through Grad-CAM, it was observed that the model sometimes makes decisions based on bony structures (ribs, clavicle) instead of lung tissue itself, which opens up space for further research and improvement.

AUTHOR: Ivona Pranjić
2025./2026.
