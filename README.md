# Extractive Text Summarization using BERT

## Project Overview
This project aims to implement a text summarization model utilizing BERT for token classification to extract symptoms from text data.

## Dependencies
The project requires the following libraries:
- `pandas`
- `numpy`
- `nltk`
- `contractions`
- `transformers`
- `datasets`
- `torch`
- `rouge_score`

## Key Steps in the Project

1. **Data Cleaning**:
   - The `text_cleaner` function processes each post to remove stopwords, contractions, and special characters, resulting in a cleaned text.

2. **Label Preparation**:
   - The `prepare_labels` function generates labels based on the presence of negative words in the cleaned text. If a negative word is found, it marks the corresponding label and the preceding words.

3. **Data Splitting**:
   - The dataset is shuffled and split into training, validation, and test sets.

4. **Dataset Conversion**:
   - The cleaned text and labels are converted into a format suitable for BERT training.

5. **Model Training**:
   - A BERT model for token classification is instantiated and trained using the Hugging Face `Trainer` API with defined training arguments. The model is saved for future use.

6. **Extractive Summary Generation**:
   - The `extractive_summary` function tokenizes input text and uses the trained model to identify and extract relevant sentences that contain negative sentiments.

7. **Evaluation**:
   - The ROUGE metric is used to evaluate the performance of the summarization model against reference summaries in the test set.

## Results
The average ROUGE scores are computed to evaluate the effectiveness of the summarization model on the test set.

## Usage
To run the project:
1. Install the required libraries.
2. Ensure the dataset files are in the correct path.
3. Execute the code in a Python environment with GPU support for optimal performance.

## Conclusion
This project demonstrates the effectiveness of using BERT for extractive summarization, providing insights into the emotional content of text data.

## Ethical Considerations
Due to the sensitive nature of the content and privacy concerns, the dataset cannot be shared publicly.
