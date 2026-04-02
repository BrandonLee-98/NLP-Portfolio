# NewsBot Intelligence System (ITAI 2373 Midterm)

##  Project Overview
This is an end-to-end NLP pipeline designed to automate media monitoring and business intelligence. Instead of manually sorting through thousands of articles, this system cleans, categorizes, and extracts key facts (entities and sentiment) automatically. 

I built this as a solo project to demonstrate how integrated NLP techniques—from [preprocessing](https://colab.research.google.com/drive/15OwHv6RTp5Rt6QDC4Ig3pyj0Ra_TwoqV#scrollTo=9063) to [Multi-Class Classification](https://colab.research.google.com/drive/15OwHv6RTp5Rt6QDC4Ig3pyj0Ra_TwoqV#scrollTo=6000)—can solve the "information overload" problem in sectors like public safety and legal research.

## Technical Features
* **Preprocessing:** Custom pipeline to strip noise, tokenize, and lemmatize text for cleaner model input.
* **Linguistic Analysis:** [POS tagging](https://colab.research.google.com/drive/15OwHv6RTp5Rt6QDC4Ig3pyj0Ra_TwoqV#scrollTo=8126) and [Syntax parsing](https://colab.research.google.com/drive/15OwHv6RTp5Rt6QDC4Ig3pyj0Ra_TwoqV#scrollTo=7580) used to identify category-specific writing styles.
* **Sentiment & Entities:** Integrated [VADER sentiment scores](https://colab.research.google.com/drive/15OwHv6RTp5Rt6QDC4Ig3pyj0Ra_TwoqV#scrollTo=6884) and [spaCy NER](https://colab.research.google.com/drive/15OwHv6RTp5Rt6QDC4Ig3pyj0Ra_TwoqV#scrollTo=3807) (PERSON, ORG, GPE) as predictive features.
* **Optimized Classifier:** A [Logistic Regression model](https://colab.research.google.com/drive/15OwHv6RTp5Rt6QDC4Ig3pyj0Ra_TwoqV#scrollTo=6000) tuned via [GridSearchCV](https://colab.research.google.com/drive/15OwHv6RTp5Rt6QDC4Ig3pyj0Ra_TwoqV#scrollTo=5079) ($C=10$).

## Dataset & Results
* **Data:** 3,000 articles sampled from the HuffPost News Category dataset. I chose a larger sample to better prepare for the semester's final project.
* **Accuracy:** Achieved **48.5% accuracy** across 41 categories. This was boosted significantly after [merging overlapping categories](https://colab.research.google.com/drive/15OwHv6RTp5Rt6QDC4Ig3pyj0Ra_TwoqV#scrollTo=6085) like 'Healthy Living' and 'Wellness.'

## How to Run
1. Open the [Midterm_NewsBot_BrandonMatias.ipynb](https://colab.research.google.com/drive/15OwHv6RTp5Rt6QDC4Ig3pyj0Ra_TwoqV) in Google Colab.
2. Upload your `kaggle.json` to fetch the dataset.
3. Run all cells to see the full pipeline, from raw JSON to the final confusion matrix and entity analysis.

---
**Author:** Brandon Lee  
**Course:** ITAI 2373 - Natural Language Processing  
**Institution:** Houston Community College
