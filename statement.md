# Project Statement: AI-Based Disease Diagnosis System

## Problem Statement
Early identification of a likely illness based on common symptoms can help people decide
whether and how urgently to seek medical care. However, manually cross-referencing a set
of symptoms against possible diseases is time-consuming and error-prone for a
non-specialist. This project addresses that problem by building a simple, rule-learned
Machine Learning model that takes a small set of yes/no symptom inputs (fever, cough,
headache, fatigue, nausea) and predicts the most likely associated disease, giving users
a quick, preliminary indication before consulting a doctor.

## Scope of the Project
- A **Command Line Interface (CLI)** application written in Python.
- Uses a small, labeled CSV dataset of symptom combinations mapped to a disease label
  (e.g., Flu, Cold, Malaria, Allergy, COVID-19, Migraine, Dengue, Fatigue).
- Trains a **Decision Tree Classifier** (via scikit-learn) on the dataset at runtime,
  splitting it into training and test sets to report a basic accuracy score.
- Accepts five binary (0/1) symptom inputs from the user through the console and returns
  a single predicted disease label.
- Intended as an educational/demonstration project showing an end-to-end ML workflow
  (data loading → training → prediction → output), not a certified medical tool.
- Out of scope: a graphical or web interface, large-scale/real-world medical datasets,
  multi-symptom severity scoring, probability/confidence output, and any form of
  clinical validation or regulatory compliance.

## Target Users
- **Students and learners** exploring how a basic supervised ML classification pipeline
  works end-to-end.
- **Instructors/evaluators** (e.g., for the Vityarthi AI & ML coursework) reviewing a
  practical demonstration of ML concepts.
- **General users** curious about a lightweight, non-clinical symptom-checking demo, with
  the understanding that results are illustrative only and not a substitute for
  professional medical advice.

## High-Level Features
1. **Symptom-based input collection** — Prompts the user for five common symptoms
   (fever, cough, headache, fatigue, nausea) as simple 0/1 responses.
2. **Automated model training** — Loads `dataset.csv`, splits it into training/testing
   subsets, and trains a Decision Tree Classifier each time the program runs.
3. **Accuracy reporting** — Displays the model's accuracy on the held-out test split so
   users can gauge how reliable the current prediction is likely to be.
4. **Disease prediction** — Uses the trained model to predict and display the most likely
   disease based on the entered symptoms.
5. **Input validation** — Handles invalid (non 0/1) input gracefully with an error
   message instead of crashing.
6. **Medical disclaimer** — Reminds the user that the prediction is basic/preliminary and
   that a doctor should be consulted for an actual diagnosis.
