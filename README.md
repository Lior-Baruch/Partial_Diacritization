# Partial Diacritization in Hebrew: A Dual Model Approach for Text Disambiguation

## Introduction

This repository details the work of Lior Baruch and Ben Catalan from Reichman University on applying partial diacritization to Hebrew text. The project involves the development of two distinct models—one with lookahead and one without—to predict diacritization. Additionally, a dual model approach provides partial diacritization only when the two models disagree, favoring the lookahead model's prediction. The project is inspired by the paper "How Much Does Lookahead Matter for Disambiguation? Partial Arabic Diacritization Case Study" by Saeed Esmail, Kfir Bar, and Nachum Dershowitz.

## Repository Contents

### AlephBERT-main/AlephBERT-main
- **Modified AlephBERT**: This folder contains a modified version of the AlephBERT model, tailored to our specific requirements, including changes in vocabulary as described in the paper.

### data
- **Dicta Books JSON**: The `books.json` file in this directory contains the JSON used to download the Dicta books dataset, essential for training and testing the models.

### full-sentence-final-models
- **Full-Sentence Models (With Lookahead)**: This folder holds the saved final models for the Full-Sentence approach, which considers the entire sentence context, including loss and accuracy history for each epoch.

### reading-direction-final-models
- **Reading Direction Models (Without Lookahead)**: Here, you will find the saved final models for the Reading Direction approach, which emulates natural human reading patterns, along with loss and accuracy history for each epoch.

### plots
- **Visualizations**: This directory houses various plots related to the project, including confusion matrices and loss/accuracy histories.

### Additional Files
- **Partial_Dicritization_DualModel_LSTM.ipynb**: The main Jupyter notebook containing all the code, including the two main models, dual model strategy, grid search, training, and evaluation.
- **transformer_attempt.ipynb**: A notebook detailing our attempts with the Transformer architecture.
- **From Arabic to Hebrew - Looking Ahead So We Dont Fall Behind in Diacritization.pdf**: The research paper detailing our methodology, experiments, and results.
- **.gitignore**: A file specifying untracked files that Git should ignore.
- **README.md**: This file, providing an overview of the repository.

## Conclusion

Our dual-model strategy for partial diacritization in Hebrew represents a groundbreaking approach to text disambiguation. By leveraging the synergy between a lookahead model and a reading-direction model, we have achieved a balanced and effective solution for Hebrew text processing.

## Contact and Acknowledgments

For further inquiries, collaboration, or information, please contact the authors. This project was conducted as part of an NLP course supervised by Kfir Bar at Reichman University.
