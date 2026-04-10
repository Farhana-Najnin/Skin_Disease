# Skin Disease Detection System

## Overview
This project is a skin disease detection system built using a Convolutional Neural Network (CNN). It takes a skin image as input and predicts the most likely disease class along with a confidence score. The system also provides simple guidance such as recommendations, next steps, and basic care tips. The application includes a FastAPI backend for handling predictions and a Streamlit interface for user interaction.

## Dataset Information
The dataset used in this project is collected from Kaggle ("Skin diseases image dataset"). :contentReference[oaicite:0]{index=0}  

- Total images: ~27,000+  
- Number of classes: 10 skin disease categories  
- Data is organized into separate folders for each disease class  

Example classes include:
- Eczema  
- Melanoma  
- Atopic Dermatitis  
- Basal Cell Carcinoma (BCC)  
- Melanocytic Nevi  
- Benign Keratosis  
- Psoriasis and related diseases  
- Fungal infections  
- Viral infections  

The dataset is used to train the CNN model for multi-class classification.

## Procedure / How the System Works
Step 1: Image Input  
The user uploads a skin image through the Streamlit interface or API.

Step 2: Image Preprocessing  
The image is resized to the required input size, normalized, and converted into tensor format for the model.

Step 3: Model Prediction  
A trained CNN model processes the image and generates probabilities for each class. The class with the highest probability is selected as the predicted disease.

Step 4: Confidence Score  
The probability of the predicted class is returned as the confidence score.

Step 5: Result Generation  
The system returns the predicted disease name, confidence score, and basic recommendations (rule-based).

## API Endpoint
POST `/analyze_skin`

Input:
- Image file (JPG/PNG)

Output:
```json
{
  "disease": "Predicted Class",
  "confidence": 0.85,
  "recommendations": "...",
  "next_steps": "...",
  "tips": "..."
}
