# Sentiment-Analysis-of-Pidgin-English-using-DistilBERT


This Python script is designed for the task of classifying Pidgin language text into various sentiment categories using a DistilBert model. It covers the entire workflow from data preparation to model training and evaluation.

## Setup

To run this script, ensure you have the following libraries installed:
- `transformers`
- `datasets`
- `pandas`
- `evaluate`
- `accelerate`

You can install these packages using pip:
```bash
pip install transformers datasets pandas evaluate accelerate
```

## 1. Data Preparation

The script starts by loading training, development, and test datasets from TSV files from  [SemEval-2023 Task 12: Sentiment Analysis for African Languages](https://github.com/afrisenti-semeval/afrisent-semeval-2023). It then preprocesses these datasets by mapping textual labels to numerical values for model compatibility.

## 2. Dataset Conversion and Tokenization

The dataframes are converted to Hugging Face's `datasets` format. Then, text data is tokenized using `DistilBertTokenizer` for processing by the DistilBert model.

## 3. Model Initialization and Training

The script initializes a DistilBert model for sequence classification with three labels. Training arguments, such as batch size, number of epochs, learning rate, and evaluation strategies, are set up for model training.

## 4. Training and Evaluation

The model is trained using the `Trainer` class from the transformers library. After training, the model is evaluated on the development dataset, and various metrics like F1 scores and accuracy are computed.

## 5. Usage

To run the script, simply execute it in a Python environment after setting up the necessary libraries and data files. Ensure that the data files (`pcm_train.tsv`, `pcm_dev.tsv`, `pcm_test.tsv`) are present in the same directory as the script.

## 6. Additional Notes

- The script is structured for easy modification and scaling.
- Comments and markdowns within the script provide further guidance on each section.

## Authors
- Abdulkadir Bala Richard.
- Chijioke Onyeka Ahanwa.
- David Osawese Okundigie.

## License

MIT
