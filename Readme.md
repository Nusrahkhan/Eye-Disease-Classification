Eye Disease Classification using Deep Learning

🎯 Overview
This project implements an end-to-end machine learning pipeline for multi-class classification of eye diseases. The model can identify four different conditions from retinal fundus images:

Cataract - Clouding of the eye's natural lens
Diabetic Retinopathy - Diabetes-related damage to retinal blood vessels
Glaucoma - Optic nerve damage often caused by high eye pressure
Normal - Healthy eyes with no detected pathology

The system achieves 80-83% validation accuracy with minimal overfitting, making it suitable for preliminary screening and triage in clinical workflows.
🚀 Key Features
✅ High Accuracy: Achieves ~80-83% validation accuracy with proper generalization
✅ Fast Inference: Real-time predictions in milliseconds
✅ Regularized Training: Dropout layers prevent overfitting
✅ Comprehensive Evaluation: Detailed metrics and visualization tools
📊 Model Architecture
The model is based on the classic LeNet-5 architecture, adapted for medical image classification:
Input (28x28x1 grayscale) 
    ↓
Conv2D (6 filters, 5x5) + Tanh
    ↓
AveragePooling2D (2x2)
    ↓
Conv2D (16 filters, 5x5) + Tanh
    ↓
AveragePooling2D (2x2)
    ↓
Flatten
    ↓
Dense (120 units) + Tanh + Dropout(0.3)
    ↓
Dense (84 units) + Tanh + Dropout(0.3)
    ↓
Dense (4 units) + Softmax
