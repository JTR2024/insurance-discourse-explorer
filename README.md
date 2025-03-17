# Insurance Discourse Explorer
### A Generative AI-Powered Sentiment Analysis Tool

This project demonstrates an end-to-end process of building an NLP and Generative AI solution for analyzing insurance-related discussions. It uses **synthetic data** designed to mimic typical Reddit comments about insurance topics such as auto insurance, claims, premiums, and customer service experiences.

---

## Project Overview

The **Insurance Discourse Explorer** analyzes sentiment patterns in insurance-related discussions using a combination of traditional NLP techniques and modern generative AI approaches (specifically GPT-4o). This repository serves as a portfolio demonstration of data science and AI capabilities relevant to the insurance industry.

---

## Key Features

- **Synthetic Data Generation**: Mimics insurance-related discussions without relying on a real Reddit API  
- **Data Cleaning & Preprocessing**: Pipeline for text normalization, feature engineering, and basic EDA  
- **GPT-4o Powered Sentiment Analysis**: Automated classification (Positive, Negative, Neutral) with optional rationales  
- **Topic Extraction**: Identify recurring insurance topics (e.g., claims, coverage, premiums)  
- **Interactive Visualizations**: Bar charts, time-series plots, and word clouds  
- **(Optional) RAG Implementation**: Retrieval-Augmented Generation for Q&A on synthetic data  

---

## Note on Data

This project uses **synthetic** data rather than actual Reddit comments. This approach ensures:

- Complete reproducibility without any API dependencies  
- Consistent results for demonstration  
- Avoidance of privacy or data-licensing concerns  
- Focus on technical implementation rather than data acquisition  

---

## Technologies Used

- **Python**  
- **Pandas & NumPy** for data manipulation  
- **Matplotlib & Seaborn** for visualizations  
- **WordCloud** for quick text cloud generation  
- **OpenAI API (GPT-4o)** for sentiment analysis and text generation  
- **(Optional) Streamlit** for interactive dashboards  
- **(Optional) FAISS / sentence-transformers** for advanced retrieval  

---

## Project Structure

├── notebooks/                   # Jupyter notebooks for each project step
├── data/
│   ├── synthetic_insurance_comments.csv
│   ├── processed_insurance_comments.csv
│   ├── analyzed_insurance_comments.csv
│   └── visualizations/          # Saved plots from Step 6
├── src/                         # (Optional) Reusable Python modules
├── app.py                       # (Optional) Streamlit app
├── requirements.txt             # Dependencies for environment
├── README.md                    # This file
└── …

---

## Getting Started

### 1. Open the Project in Google Colab

1. Go to [https://colab.research.google.com/](https://colab.research.google.com/)  
2. Select **File > Open Notebook**  
3. Choose **GitHub** tab  
4. Enter the repository URL (e.g., `https://github.com/JTR2024/insurance-discourse-explorer`)  
5. Select the desired notebook from the list  

### 2. Set Up the Environment

Install necessary packages in a Colab cell:

```python
!pip install openai langchain faiss-cpu sentence-transformers streamlit vaderSentiment bertopic wordcloud

import os
os.environ["OPENAI_API_KEY"] = "your-api-key-here"

4. Run the Notebooks

The workflow is broken into multiple steps, each in its own notebook:
	1.	Step 1: Environment Setup and Configuration
	2.	Step 2: Synthetic Data Generation
	3.	Step 3: Data Cleaning & Preprocessing
	4.	Step 4: GPT-4o-based Sentiment Classification
	5.	Step 5: Retrieval-Augmented Generation (RAG) (optional advanced step)
	6.	Step 6: Visualizations (and an optional simple dashboard)

Follow the instructions within each notebook to proceed in order.


Viewing the Visualizations

In Step 6, we generate and display the plots inline within the notebook itself. We also save copies of those .png images to data/visualizations/.
	•	Inline: After running Step 6, scroll down in the notebook to see the bar charts, word clouds, etc.
	•	PNG Files: You can find them in the data/visualizations/ folder. If desired, commit these images to your GitHub repo so viewers can access them easily.

(Optional) Running the Streamlit App

If you prefer an interactive UI, you can install and run streamlit. For example:

streamlit run app.py

	•	In Colab, additional steps (e.g., using ngrok) may be required to expose the app URL.
	•	Locally, you can simply run the above command in your project directory and open the local URL.

Future Enhancements
	•	Use Real Data: Replace synthetic data with actual Reddit or user feedback, if licensing and privacy allow.
	•	Advanced Modeling: Experiment with domain-specific fine-tuning or advanced topic modeling.
	•	Enhanced Dashboards: Expand the Streamlit interface for deeper exploration or user-driven queries.
	•	Multi-class or Aspect-based Sentiment: Extend beyond simple Positive/Neutral/Negative classification.

---

## 2) **Step 6 Notebook Section** (Markdown + Code)

Below is the **final** version of Step 6, which:

- Displays each plot **inline** in Colab.  
- Saves `.png` copies to `data/visualizations/`.  
- *Does NOT* zip or download automatically—everything stays in the notebook.  

Just paste the Markdown and code into your “Step 6” notebook cells.

### **Markdown for Step 6**

```markdown
# Step 6: Visualizations

## Overview
In this final step, we will create a series of plots to illustrate key insights from our synthetic insurance discussions. These visualizations will help us see how sentiment is distributed across companies, topics, and over time. We’ll also generate word clouds for each sentiment category.

### Objectives
1. Show overall sentiment distribution  
2. Examine sentiment by top companies and top topics  
3. Plot monthly comment volume by sentiment  
4. Generate word clouds highlighting the most common words within each sentiment category  

### Approach
- Use `matplotlib` and `seaborn` to create bar charts, stacked charts, and more.
- Display each chart **inline** (`plt.show()`) so you can see it right in the notebook.
- Save each chart as a `.png` in `data/visualizations/` if needed for reference or inclusion in a dashboard.

---
