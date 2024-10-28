# Toxic Comment Detection for Wikishop

This project aims to develop a machine learning model to detect toxic comments in user-generated content for the online store "Wikishop." By comparing traditional TF-IDF vectorization with advanced BERT embeddings, the model classifies comments as either toxic or neutral with the goal of achieving an F1 score of at least 0.75.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Description](#data-description)
- [Approaches](#approaches)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
Wikishop is introducing a wiki-editing feature that allows users to edit and comment on product descriptions. To ensure a positive user experience, this project builds a tool to automatically identify toxic comments and send them for moderation.

## Data Description
The dataset used in this project is `toxic_comments.csv`, containing:
- **text**: the comment text.
- **toxic**: the target label, where `1` indicates a toxic comment, and `0` indicates a neutral comment.

## Approaches
Two main approaches were used to classify comments:
1. **TF-IDF Vectorization**: A traditional approach, paired with `Logistic Regression` and `CatBoost`.
2. **BERT Embeddings**: A contextual approach using pre-trained BERT embeddings with `Logistic Regression` and `CatBoost`.

## Results
| Approach               | Model              | F1 Score |
|------------------------|--------------------|----------|
| TF-IDF + Logistic Regression | 0.728 |
| TF-IDF + CatBoost     | 0.738 |
| BERT + Logistic Regression | 0.770 |
| BERT + CatBoost       | 0.755 |

Using BERT embeddings improved model performance, with the highest F1 score achieved by Logistic Regression at 0.770.

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/toxic-comment-detection.git
    cd toxic-comment-detection
    ```
2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. **Prepare the Dataset**: Ensure `toxic_comments.csv` is in the root directory.
2. **Run the Script**: Execute the main script to train and evaluate models.
    ```bash
    python main.py
    ```
3. **Evaluate Results**: The script will output F1 scores for each approach and model.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request to propose changes.

## License
This project is licensed under the MIT License.
