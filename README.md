# RAG Evaluator

## Overview

RAG Evaluator is a Python library for evaluating Retrieval-Augmented Generation (RAG) systems. It provides various metrics to evaluate the quality of generated text against reference text.

## Installation

You can install the library using pip:

```bash
pip install rag-evaluator
```

## Usage

Here's how to use the RAG Evaluator library:

```python
from rag_evaluator import RAGEvaluator

# Initialize the evaluator
evaluator = RAGEvaluator()

# Input data
question = "What are the causes of climate change?"
response = "Climate change is caused by human activities."
reference = "Human activities such as burning fossil fuels cause climate change."

# Evaluate the response
metrics = evaluator.evaluate_all(question, response, reference)

# Print the results
print(metrics)
```

## Streamlit Web App

To run the web app:

- cd into streamlit app folder.
- Create a virtual env
- Activate
- Install all dependencies
- and run
```
streamlit run app.py
```

## Metrics

The following metrics are provided by the library:

- **BLEU**: Measures the overlap between the generated output and reference text based on n-grams.
- **ROUGE-1**: Measures the overlap of unigrams between the generated output and reference text.
- **BERT Score**: Evaluates the semantic similarity between the generated output and reference text using BERT embeddings.
- **Perplexity**: Measures how well a language model predicts the text.
- **Diversity**: Measures the uniqueness of bigrams in the generated output.
- **Racial Bias**: Detects the presence of biased language in the generated output.

## Testing

To run the tests, use the following command:

```
python -m unittest discover -s rag_evaluator -p "test_*.py"
```
