# English-to-Hindi Text Translation Model

This project is an English-to-Hindi text translation model built using TensorFlow and Keras. It leverages a Transformer architecture to provide accurate translations and includes preprocessing, tokenization, training, and evaluation steps.

## Features

- **Text Preprocessing:** Cleans and preprocesses the input text for training.
- **Vectorization:** Converts text into numerical vectors using Keras TextVectorization.
- **Transformer Model:** Implements a Transformer-based model for sequence-to-sequence translation.
- **Training:** Trains the model using prepared datasets with EarlyStopping and ReduceLROnPlateau callbacks.
- **Evaluation:** Calculates BLEU scores to evaluate the translation quality.

## Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/english-to-hindi-translation.git
    cd english-to-hindi-translation
    ```

2. **Create and activate a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Prepare the data:**
    - Download the dataset and place it in the project directory.
    - The dataset should be a CSV file with columns for English and Hindi sentences.

2. **Run the script:**
    ```bash
    python translation_model.py
    ```

3. **Model Training:**
    - The script will preprocess the data, tokenize the sentences, and train the Transformer model.
    - The trained model weights will be saved as `eng-hin.h5`.

4. **Evaluate the model:**
    - The script will also evaluate the model on a test dataset and print the BLEU score.

## Code Overview

- **`translation_model.py`:** The main script that includes all preprocessing, model training, and evaluation logic.

### Core Functions

- **`preprocess_text(df)`:** Cleans and preprocesses the text data.
- **`decode_sequence(input_sentence)`:** Decodes input sentences using the trained model.
- **`format_dataset(eng, hin)`:** Formats the dataset for training.
- **`make_dataset(df)`:** Creates TensorFlow datasets from the dataframe.
- **`custom_standardization(input_string)`:** Custom standardization function for text vectorization.
- **`PositionalEmbedding`:** Layer for positional embeddings in the Transformer model.
- **`TransformerEncoder`:** Encoder layer of the Transformer model.
- **`TransformerDecoder`:** Decoder layer of the Transformer model.

## Dependencies

- os
- pickle
- pandas
- numpy
- random
- string
- re
- nltk
- tensorflow
- keras

We hope this model helps you achieve high-quality English-to-Hindi translations!
