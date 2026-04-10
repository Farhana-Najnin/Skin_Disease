# Skin Disease Detection System

## Overview
This project is a skin disease detection system built using a Convolutional Neural Network (CNN). It takes a skin image as input and predicts the most likely disease class along with a confidence score. The system also provides simple guidance such as recommendations, next steps, and basic care tips. The application includes a FastAPI backend for handling predictions and a Streamlit interface for user interaction.

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
Streamlit UI

Upload Interface


Image Upload Example


Prediction Result


Recommendations Output


Another Example


API Documentation

Model Evaluation

Confusion Matrix


Evaluation includes Confusion Matrix and Classification Report.

Project Files
skindiseaseupdated.py → FastAPI backend
streamlit_app.py → Streamlit interface
skinDiseaseUpdated.ipynb → Model training notebook
requirements.txt → Dependencies
How to Run

Install dependencies:
pip install -r requirements.txt

Run FastAPI backend:
uvicorn skindiseaseupdated:app --reload

Run Streamlit app:
streamlit run streamlit_app.py
