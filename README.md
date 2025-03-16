# Insurance Discourse Explorer: A Generative AI-Powered Sentiment Analysis

## Project Overview
This project leverages Generative AI and Natural Language Processing techniques to analyze real-world insurance discussions from social media platforms (Reddit). It demonstrates end-to-end data science workflow capabilities relevant to the insurance industry, from data collection through analysis to visualization.

### Key Features
- **Data Collection**: Scraping insurance-related discussions from Reddit using Pushshift API
- **Sentiment Analysis**: Utilizing GPT-4 to classify posts into positive, negative, or neutral sentiments
- **Topic Extraction**: Identifying key insurance topics from unstructured text
- **Retrieval-Augmented Generation (RAG)**: Implementing a vector database for efficient querying of insurance discussions
- **Interactive Visualization**: Building a Streamlit dashboard to explore sentiments and topics

## Technologies Used
- **Python**: Core programming language
- **Pandas/NumPy**: Data manipulation and analysis
- **OpenAI API**: GPT-4 integration for advanced NLP tasks
- **FAISS**: Vector database for similarity search
- **Streamlit**: Interactive web application development
- **Matplotlib/Seaborn**: Data visualization

## Project Structure
```
Insurance-Discourse-Explorer/
├── notebooks/
│   └── insurance_discourse_analysis.ipynb  # Main analysis notebook
├── app/
│   ├── app.py                             # Streamlit application
│   └── utils.py                           # Helper functions
├── data/
│   ├── raw/                               # Raw scraped data
│   └── processed/                         # Cleaned and processed data
├── models/
│   └── vector_store/                      # FAISS vector database
├── requirements.txt                       # Project dependencies
└── README.md                              # Project documentation
```

## Getting Started
1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt`
3. Run the Jupyter notebook for detailed analysis
4. Launch the Streamlit app: `streamlit run app/app.py`

## Business Applications
This project demonstrates capabilities directly applicable to insurance industry challenges:
- **Customer Sentiment Analysis**: Understanding public perception of insurance products and services
- **Competitive Intelligence**: Analyzing discussions about competitors
- **Product Development**: Identifying pain points and opportunities from real customer feedback
- **Risk Assessment**: Detecting emerging concerns in the insurance landscape

## Future Enhancements
- Expand data sources to include Twitter, news articles, and other platforms
- Implement more sophisticated domain adaptation for commercial insurance
- Develop automated reporting for sentiment trends over time
- Add additional NLP models for comparative analysis

## License
MIT

## Contact
[John Russell](jtruss.info@gmail.com) 
