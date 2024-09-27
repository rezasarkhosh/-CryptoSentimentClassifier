# 🚀 Bitcoin Sentiment Analysis

This repository contains a project that performs **Sentiment Analysis** on Bitcoin market discussions using a **Logistic Regression model** and text classification techniques.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Usage](#usage)
  - [Sentiment Labeling](#sentiment-labeling)
  - [Training a Logistic Regression Model](#training-a-logistic-regression-model)
  - [Predicting Sentiment](#predicting-sentiment)
- [Technologies Used](#technologies-used)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project automates the process of:
1. **Labeling** Bitcoin market analysis sentences as **Positive**, **Negative**, or **Neutral** based on predefined word sets.
2. **Training a Logistic Regression Model** on labeled Bitcoin market discussions to classify new text into sentiment categories.
3. **Predicting Sentiment**: Takes a user prompt and predicts the sentiment.

## Features

- **Sentiment Labeling**: Automatically labels sentences based on predefined positive and negative words.
- **Logistic Regression Model**: Uses TF-IDF vectorization to train and evaluate a Logistic Regression model.
- **Prediction Functionality**: Allows user input for real-time sentiment prediction based on trained models.

### Required Files

1. **`BTC_normalized.txt`**: Contains Bitcoin-related sentences for analysis.
2. **`BTC_labeled.txt`**: A file with sentences labeled as Positive, Negative, or Neutral.

## Usage

### Sentiment Labeling

The **labeling** component assigns sentiment labels to Bitcoin market analysis data based on predefined sets of positive and negative words.

Run the labeling script:

```bash
python label_sentences.py
```

This will save the labeled data to:
- `data/BTC_labeled.txt`

### Training a Logistic Regression Model

The Logistic Regression model is trained on the labeled dataset using TF-IDF for feature extraction.

Run the training script:

```bash
python train_model.py
```

This will output the model's performance in terms of precision, recall, and F1-score for each sentiment category (Positive, Neutral, and Negative).

### Predicting Sentiment

To predict the sentiment of a new sentence, use the following script. The user can enter a sentence, and the model will predict its sentiment:

```bash
python predict_sentiment.py
```

You will be prompted to input a sentence, and the model will output its predicted sentiment (Positive, Neutral, or Negative).

## Technologies Used

- **Natural Language Processing**: `nltk`, `scikit-learn`
- **Machine Learning Models**: `Logistic Regression`
- **Text Representation**: `TF-IDF Vectorization`
- **Other Tools**: `pandas`, `numpy`, `matplotlib`

## Future Improvements

- **Enhanced Sentiment Analysis**: Incorporate deep learning models such as BERT for more accurate sentiment classification.
- **Additional Features**: Add support for multi-class sentiment labeling or fine-tune on domain-specific datasets.
- **Interactive Web Interface**: Build a real-time prediction interface using **Streamlit** or **Flask**.
- **Visualization**: Add visualizations of sentiment trends in Bitcoin discussions.

## Contributing

Contributions are welcome! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new feature branch (`git checkout -b feature/new-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/new-feature`).
5. Open a Pull Request.

Please ensure that your code adheres to the project's style guidelines and is well-tested.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

