# Insurance Discourse Explorer
## A Generative AI-Powered Sentiment Analysis Tool

This project demonstrates an end-to-end process of building an NLP and Generative AI solution for analyzing insurance-related discussions. It uses synthetic data designed to mimic typical Reddit comments about insurance topics such as auto insurance, claims, premiums, and customer service experiences.

## Project Overview
The Insurance Discourse Explorer analyzes sentiment patterns in insurance-related discussions using a combination of traditional NLP techniques and modern generative AI approaches (specifically GPT-4o). This repository serves as a portfolio demonstration of data science and AI capabilities relevant to the insurance industry.

## Key Features
- **Synthetic Data Generation**: Mimics insurance-related discussions without relying on a real Reddit API.
- **Data Cleaning & Preprocessing**: Pipeline for text normalization, feature engineering, and basic EDA.
- **GPT-4o Powered Sentiment Analysis**: Automated classification (Positive, Negative, Neutral) with optional rationales.
- **Topic Extraction**: Identifies recurring insurance topics (e.g., claims, coverage, premiums).
- **Interactive Visualizations**: Bar charts, time-series plots, and word clouds to illustrate key insights.
- **(Optional) RAG Implementation**: Retrieval-Augmented Generation for more intelligent question answering on synthetic data.

## Note on Data
This project uses synthetic data rather than actual Reddit comments. This approach ensures:
- Complete reproducibility without any API dependencies
- Consistent results for demonstration
- Avoidance of privacy or data-licensing concerns
- Focus on technical implementation rather than data acquisition

## Technologies Used
- Python
- Pandas & NumPy for data manipulation
- Matplotlib & Seaborn for visualizations
- WordCloud for quick text cloud generation
- OpenAI API (GPT-4o) for sentiment analysis and text generation
- (Optional) FAISS / sentence-transformers for advanced retrieval

## Project Structure

.
├── notebooks/                  # Jupyter notebooks for each project step
├── data/
│   ├── synthetic_insurance_comments.csv
│   ├── processed_insurance_comments.csv
│   ├── analyzed_insurance_comments.csv
│   └── visualizations/         # Saved plots from Step 6
├── src/                       # (Optional) Reusable Python modules
├── requirements.txt           # Dependencies for environment
├── README.md                  # This file
└── …


## Getting Started
1. **Open the Project in Google Colab**
   a. Go to https://colab.research.google.com/
   b. Select `File > Open Notebook`
   c. Choose the `GitHub` tab
   d. Enter the repository URL (e.g., https://github.com/JTR2024/insurance-discourse-explorer)
   e. Select the desired notebook from the list

2. **Set Up the Environment**
   In a Colab cell, install the necessary packages:

!pip install openai langchain faiss-cpu sentence-transformers vaderSentiment bertopic wordcloud


3. **Configure the OpenAI API Key**
```python
import os
os.environ["OPENAI_API_KEY"] = "your-api-key-here"

   (Alternatively, use Colab’s secrets manager for improved security.)
Run the Notebooks
The project is broken into multiple steps, each in its own notebook:
Step 1: Environment Setup and Configuration

Step 2: Synthetic Data Generation

Step 3: Data Cleaning & Preprocessing

Step 4: GPT-4o-based Sentiment Classification

Step 5: Retrieval-Augmented Generation (RAG) (optional advanced step)

Step 6: Visualizations (and an optional simple dashboard)
Follow the instructions in each notebook to proceed in order.

Viewing the Visualizations
In Step 6, we:
Display each plot inline in the notebook (bar charts, word clouds, etc.).

Save copies of those images (.png) into the data/visualizations/ folder.

If you’d like to commit those images to your GitHub repo, just download them from Colab and place them in data/visualizations/.
Future Enhancements
Use Real Data: Replace synthetic data with actual Reddit or user feedback, if licensing and privacy allow.

Advanced Modeling: Experiment with domain-specific fine-tuning or advanced topic modeling.

Multi-class or Aspect-based Sentiment: Extend beyond simple Positive/Neutral/Negative classification.


