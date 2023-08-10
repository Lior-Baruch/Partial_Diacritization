# **Punctuation Restoration in Hebrew: A Dual Model Approach**

This Jupyter notebook, a continuation of the research carried out at Reichman University by Lior Baruch and Ben Catalan, offers a sophisticated strategy for Hebrew punctuation (or "nikud") restoration. Drawing inspiration from the paper "How Much Does Lookahead Matter for Disambiguation? Partial Arabic Diacritization Case Study", this notebook adapts the principles to Hebrew, synergizing two distinct models - a Transformer and an LSTM. The culmination of this effort is to achieve optimal nikud placement, enhancing both readability and comprehension. This work was undertaken as part of the NLP course guided by Kfir Bar.

## **Overview**

Traditional full nikud on every word in Hebrew can create a dense text layout, impeding smooth reading. To address this, the dual-model approach in this notebook strikes a balance: it provides sufficient punctuation for clarity while ensuring that the text remains effortlessly readable. This balance is achieved by focusing on ambiguous characters, which truly require nikud for disambiguation, and by leveraging the complementary strengths of both the Transformer and LSTM models.

## **Table of Contents:**

1. **Initialization and Setup**
    - Necessary pip installations.
    - Importing essential libraries.
    - Setting up seeds for reproducibility.
  
2. **Data Preprocessing**
    - Loading and extracting data with vowels and punctuations.
    - Efficiently downloading and organizing files.
    - Creating a dictionary with authors as keys and their corresponding files as values.
    - A comprehensive suite of functions for data cleaning and preprocessing.
    - Compilation of sentences into a unified CSV.

3. **Data Exploration and Analysis**
    - Constructing label-to-ID mappings.
    - Calculating label weights.
    - Comprehensive Exploratory Data Analysis (EDA) to understand the dataset's nuances.

4. **Data Preparation for Model Training**
    - Definition and implementation of a custom DataSet class.
    - Acquiring the tokenizer and a base pre-trained model (`alephbert-base`).
    - Segregating data into training, validation, and test subsets with corresponding data loaders.
    - Further EDA to ensure data readiness.

5. **Model Architecture and Training**
    - Introduction of two main models:
        - **Full-Sentence Model (Transformer with lookahead)**
        - **Reading-Direction Model (LSTM without lookahead)**
    - Detailed training dynamics for both models.

6. **Model Evaluation and Analysis**
    - Rigorous evaluation using a variety of metrics.
    - In-depth analysis functions for:
        - Full Sentence Model
        - Reading Direction Model

7. **Optimal Dual Model Strategy**
    - The dual model that integrates predictions from both primary models.
    - In situations of disagreement between the two core models, predictions from the Transformer, which considers the entire sentence context, are prioritized.

## **Conclusion**

This notebook offers a novel approach to punctuation restoration in Hebrew. By concentrating on ambiguous characters and judiciously placing nikud only where it's essential for understanding, the dual-model strategy achieves a balance between clarity and readability. It stands as a significant contribution to Hebrew text processing in the realm of NLP.

--- 

Please review the integrated README and let me know if any further adjustments or additions are needed.