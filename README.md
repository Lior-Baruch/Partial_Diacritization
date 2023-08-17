# **Punctuation Restoration in Hebrew: A Dual Model Approach**
(not done yet, will be completed in the next couple of days)

Hello, we're Lior Baruch and Ben Catalan from Reichman University. In this Jupyter notebook, we present a sophisticated strategy for Hebrew punctuation (or "nikud") restoration. Drawing inspiration from the paper "How Much Does Lookahead Matter for Disambiguation? Partial Arabic Diacritization Case Study", we adapted the principles to Hebrew, utilizing two distinct models - a Transformer and an LSTM. Our objective is to achieve optimal nikud placement, ensuring both readability and comprehension. This work was part of the NLP course supervised by Kfir Bar.

## **Overview**

We noticed that the traditional full nikud on every Hebrew word often results in a dense text layout, making reading a challenge. To address this, we designed a dual-model approach aiming to strike a balance: providing sufficient punctuation for clarity without overwhelming the text. By focusing on ambiguous characters that truly benefit from nikud for disambiguation, and leveraging the combined strengths of both the Transformer and LSTM models, we believe we've achieved this balance.

## **Table of Contents:**

1. **Initialization and Setup**
    - Pip installations we found necessary.
    - Libraries we used extensively.
    - Setting up seeds for reproducibility.
  
2. **Data Preprocessing**
    - Loading and extracting relevant data.
    - Efficient methods for downloading and organizing files.
    - Our approach to categorizing data by author.
    - Comprehensive data cleaning and preprocessing functions we developed.
    - Compiling sentences into a unified CSV.

3. **Data Exploration and Analysis**
    - Building label-to-ID mappings.
    - Calculating label weights.
    - Detailed Exploratory Data Analysis (EDA) to understand the dataset's nuances.

4. **Data Preparation for Model Training**
    - Implementing a custom DataSet class.
    - Incorporating the tokenizer and a base pre-trained model (`alephbert-base`).
    - Dividing data into training, validation, and test subsets.
    - Additional EDA to confirm data readiness.

5. **Model Architecture and Training**
    - Introduction to our two main models:
        - **Full-Sentence Model (Transformer with lookahead)**
        - **Reading-Direction Model (LSTM without lookahead)**
    - Our approach to training both models.

6. **Model Evaluation and Analysis**
    - Evaluating the models using diverse metrics.
    - In-depth analysis functions for:
        - Full Sentence Model
        - Reading Direction Model

7. **Optimal Dual Model Strategy**
    - Our dual model that combines predictions from both primary models.
    - In cases of disagreement, we prioritized the Transformer's predictions, which consider the entire sentence context.

## **Conclusion**

We believe this notebook offers a groundbreaking approach to punctuation restoration in Hebrew. By focusing on the right characters and judiciously placing nikud, our dual-model strategy strikes the perfect balance between clarity and readability. We're proud of this contribution to Hebrew text processing in the realm of NLP.
