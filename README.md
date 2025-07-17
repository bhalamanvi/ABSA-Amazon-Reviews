**Advanced Amazon Review Analysis System**

This repository contains a sophisticated Python-based system for performing in-depth analysis of Amazon product reviews. 
The project goes beyond simple sentiment classification, incorporating multi-faceted analysis including aspect extraction, emotion detection, and graph-based fake review detection. 
It leverages state-of-the-art NLP models from the Hugging Face ecosystem, alongside network analysis and traditional machine learning techniques.

**✨ Features**

**📦 Data Loading & Preprocessing:** Efficiently loads and preprocesses massive Amazon review datasets from the McAuley-Lab/Amazon-Reviews-2023 source on Hugging Face.

**🎭 Multi-Label Emotion Analysis:** Utilizes a powerful transformer model (j-hartmann/emotion-english-distilroberta-base) to detect a range of emotions (joy, sadness, anger, fear, surprise, etc.) in review texts.

**🎯 Aspect-Based Sentiment Analysis (ABSA):**
Employs a hybrid approach to extract specific product aspects (e.g., battery life, fragrance, graphics).
Rule-Based: Uses category-specific keyword matching.
Embedding-Based: Calculates semantic similarity between review text and predefined aspects using sentence embeddings.

**🕸️ Graph-Based Fake Review Detection:**
Constructs a reviewer network using NetworkX to model relationships between users who review the same products.
Identifies suspicious "review rings" or clusters by analyzing subgraph density.
Combines network signals, text similarity, temporal burst patterns, and rating extremity to calculate a suspicious_score.

**📊 Rich Visualizations:** Generates and saves a suite of plots using Matplotlib and Seaborn to provide actionable insights, including:
Emotion distribution by category and rating.
Aspect frequency overall, by category, and by rating.
Fake review distribution and patterns.
Reviewer network graphs.
