# 🥗 NutriSage

### Smart Nutrition Assistant for Food Analysis & Personalized Meal Guidance

NutriSage is an **AI-powered smart nutrition assistant** that transforms raw food data into **clear, personalized, and actionable health insights**.
It bridges the interpretability gap in nutrition tools by explaining *what nutrients actually mean for your health*, rather than just showing numbers.

---

## 🚀 Key Highlights

* 🧠 **Interpretability-first nutrition analysis**
* 📝 **Text-based meal understanding** (natural language input)
* 🖼️ **Image-based food recognition**
* 📊 **Personalized nutrition insights & balance scoring**
* 🔍 **Food comparison, meal planning & tracking**
* 🤖 **Knowledge-driven Q&A chatbot (RAG-based)**
* 🌐 **End-to-end Streamlit web application**

---

## ❓ Problem Statement

* Poor diet quality is a leading global cause of preventable disease.
* Existing nutrition apps overwhelm users with **raw numbers** (calories, macros) without explaining their **health implications**.
* Users struggle to interpret nutrition data meaningfully.

👉 **NutriSage solves this by making nutrition data understandable, explainable, and personalized.**

---

## 💡 What Makes NutriSage Unique?

* **Beyond calorie counting** – explains *why* nutrients matter.
* **Interpretability Layer** – converts numbers into health insights, warnings, and tips.
* **Multi-modal input** – accepts both **text and food images**.
* **Nutrient Diversity Score** – measures meal balance (0–100).
* **Science-backed Q&A** – Retrieval-Augmented Generation (RAG) ensures reliable answers.
* **Realistic & practical suggestions**, not generic advice.

---

## 🎯 Core Objectives

* Translate nutrient values into **simple health-related language**
* Highlight **potential risks and benefits**
* Support **text-based and image-based meal analysis**
* Compute a **Nutrition Balance / Diversity Score**
* Assist users with **meal planning, tracking, and comparisons**
* Provide **trusted nutrition knowledge** via RAG chatbot

---

## 🏗️ System Architecture Overview

NutriSage integrates:

* Curated food datasets
* NLP-based food understanding
* Computer vision for image recognition
* Rule-based interpretability logic
* Web-powered retrieval for knowledge grounding

All components are unified through a **Streamlit-based interactive interface**.

---

## 📊 Dataset & Data Processing

### Dataset Used

* **MM-Food Dataset** (Hugging Face)
* Image–text food dataset containing:

  * Dish names
  * Ingredients
  * Portions
  * Cooking methods
  * Basic nutrition info

### Preprocessing & Curation

* Cleaned metadata and removed duplicates
* Filtered low-quality images
* Selected **10,996 high-quality food images**
* Standardized portions and nutrient values
* Created engineered features (e.g., calories per 100g)

📌 Final dataset used for model training and validation:
`MM_Food_Cleaned_Final.csv` 

---

## 🧠 Core Features

### 1️⃣ Text-Based Meal Analysis

* Accepts natural language input (e.g., *“2 cups rice with dal”*)
* Parses food names, quantities, and units
* Converts portions into grams
* Maps food items using sentence embeddings (MiniLM / SBERT)
* Computes total calories, protein, fat, and carbs

---

### 2️⃣ Interpretability Layer & Smart Insights

* Compares nutrients against daily targets (RDA-based logic)
* Labels nutrients as **low / moderate / high**
* Generates health explanations and improvement tips
* Computes **Nutrition Balance / Diversity Score (0–100)**
* Visual feedback:

  * Macro donut charts
  * RDA comparison bars
  * Metric cards

---

### 3️⃣ Image-Based Food Recognition

* Upload food images (JPG / PNG)
* EfficientNet-B3 classifier (fine-tuned on MM-Food)
* Top-k predictions with confidence scores
* High-confidence predictions auto-selected
* OCR fallback when confidence is low
* Fully integrated with text-based nutrition pipeline

---

### 4️⃣ Food Comparison Tool

* Side-by-side comparison of two foods/meals
* Standardized portion (per 100g)
* Visualized differences using bar & radar charts
* Helps users choose healthier alternatives

---

### 5️⃣ Weekly Meal Planner

* Calorie-guided meal generation
* Balanced macro distribution across days
* Smart food swaps if calorie limits are exceeded

---

### 6️⃣ Nutrition Tracker

* Saves analyzed meals with timestamps
* Tracks daily intake trends
* CSV export for further analysis

---

### 7️⃣ Knowledge-Driven Q&A Assistant (RAG Chatbot)

* Answers nutrition-related questions safely
* Uses:

  * Sentence embeddings (MiniLM)
  * Web retrieval via DuckDuckGo
  * Qwen 2.5 (3B) for answer generation
* Displays **source transparency**
* Can personalize answers using recent meal context

---

## 🧪 Models & Technologies Used

* **NLP**: Sentence Transformers (MiniLM / SBERT)
* **Computer Vision**: EfficientNet-B3
* **LLM**: Qwen 2.5 (3B)
* **Retrieval**: DuckDuckGo Search
* **Frontend**: Streamlit
* **Backend Logic**: Python (rule-based + ML pipelines)

---

## 🔮 Future Enhancements

* Improved image recognition for mixed & regional dishes
* Personalized nutrition profiles (goals, allergies, conditions)
* Expanded micronutrient coverage (fiber, sodium, vitamins)
* Smarter portion estimation from images
* Barcode scanning for packaged foods
* Reduced dependency on live web retrieval

---

## 👥 Team

* **Aaditya Kumar Dhaka**
* **Neelanjan Dutta**
  Guided by **Dr. Sathya P**

---

## 📌 Conclusion

NutriSage demonstrates how **AI, interpretability, and multi-modal understanding** can be combined to create a practical, trustworthy, and user-friendly nutrition assistant that goes beyond numbers to deliver real health value.

