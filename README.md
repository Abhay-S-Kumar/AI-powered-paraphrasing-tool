
# AI-Powered Paraphrasing Tool

## Description
This tool leverages advanced AI models to provide sophisticated text paraphrasing capabilities. Beyond simply rephrasing sentences, it integrates grammar and spelling checks to enhance the quality of the output. It also includes evaluation metrics to assess the semantic similarity and linguistic quality of the paraphrased text against the original.

## Features
-   **Text Paraphrasing**: Utilizes the T5 (Text-to-Text Transfer Transformer) model to generate alternative phrasings of input text while retaining its original meaning.
-   **Grammar and Spelling Correction**: Employs `language-tool-python` to identify and correct grammatical errors and typos in the paraphrased output.
-   **Semantic Similarity Evaluation**: Uses `Sentence-Transformers` to calculate the cosine similarity between the original and paraphrased text, ensuring the meaning is preserved.
-   **BLEU Score Calculation**: Measures the quality of the paraphrased text by comparing it to the original, focusing on n-gram overlap.
-   **ROUGE Score Calculation**: Evaluates the paraphrase quality by assessing overlap of n-grams, word sequences, and word pairs between the generated text and the original.

## Installation
To get started with the AI-Powered Paraphrasing Tool, you need to install the following Python packages. It is recommended to use a virtual environment.

```bash
pip install transformers torch sentencepiece
pip install nltk spacy language-tool-python
pip install evaluate rouge-score sacrebleu sentence-transformers
```

## How to Use

1.  **Run the script**: Execute the Colab notebook or the Python script containing the tool.
2.  **Enter text**: When prompted, enter the text you wish to paraphrase.

    Example interaction:

    ```
    Enter text to paraphrase:
    Artificial intelligence is transforming the way industries operate.
    ```

3.  **View Results**: The tool will then output the original text, the paraphrased text (after grammar correction), and the evaluation metrics.

    Expected output (example):

    ```
    Original: Artificial intelligence is transforming the way industries operate.
    Paraphrased: Artificial intelligence transforms the way industries operate.
    Semantic Similarity Score: 0.8764650225639343
    BLEU: {'bleu': 0.4518010018049224, 'precisions': [0.7, 0.5555555555555556, 0.375, 0.2857142857142857], 'brevity_penalty': 1.0, 'length_ratio': 1.1111111111111112, 'translation_length': 10, 'reference_length': 9}
    ROUGE: {'rouge1': 0.75, 'rouge2': 0.5714285714285714, 'rougeL': 0.75, 'rougeLsum': 0.75}
    ```
