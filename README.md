# Insurance Discourse Explorer

## A Generative AI-Powered Sentiment Analysis Tool

This project demonstrates an end-to-end process of building an NLP and Generative AI solution for analyzing insurance-related discussions. The project uses synthetic data designed to mimic typical Reddit comments about insurance topics such as auto insurance, claims, premiums, and customer service experiences.

### Project Overview

The Insurance Discourse Explorer analyzes sentiment patterns in insurance-related discussions using a combination of traditional NLP techniques and modern generative AI approaches (specifically GPT-4o). This repository serves as a portfolio demonstration of data science and AI capabilities relevant to the insurance industry.

### Key Features

- Synthetic data generation mimicking insurance-related discussions
- Data cleaning and preprocessing pipeline
- GPT-4o powered sentiment analysis and classification
- Topic extraction and categorization
- Interactive visualizations of sentiment trends
- (Optional) Retrieval-Augmented Generation (RAG) for intelligent querying

### Note on Data

This project uses **synthetic data** rather than actual Reddit comments. This approach ensures:
- Complete reproducibility without API dependencies
- Consistent results for demonstration purposes
- Avoidance of privacy concerns
- Focus on the technical implementation rather than data acquisition

### Technologies Used

- Python
- Pandas & NumPy for data manipulation
- OpenAI API (GPT-4o) for sentiment analysis and text generation
- Transformers library for additional NLP capabilities
- Matplotlib/Seaborn/Plotly for visualizations
- Streamlit for interactive dashboard (optional)

### Project Structure

- `notebooks/`: Jupyter notebooks with step-by-step implementation
- `data/`: Directory containing synthetic datasets
- `src/`: Source code for reusable components
- `app.py`: Streamlit application for interactive exploration (if implemented)
- `requirements.txt`: Dependencies for reproducing the environment

### Getting Started

1. **Access the Google Colab notebooks**
   - Open Google Colab: https://colab.research.google.com/
   - Go to File > Open Notebook
   - Select the "GitHub" tab
   - Enter the repository URL: https://github.com/JTR2024/insurance-discourse-explorer
   - Choose the notebook you want to run from the list

2. **Set up the Colab environment**
   - Run the following in a code cell to install any additional required packages:
   ```python
   !pip install openai langchain faiss-cpu sentence-transformers streamlit vaderSentiment bertopic
   ```

3. **Configure API keys**
   - Store your OpenAI API key securely in Colab:
   ```python
   import os
   os.environ["OPENAI_API_KEY"] = "your-api-key-here"  # Replace with your actual API key
   # Alternatively, use Colab's secrets manager for better security
   ```

4. **Run the notebooks**
   - Execute the notebooks in numerical order
   - Each notebook contains detailed explanations and code for a specific step in the pipeline

---
