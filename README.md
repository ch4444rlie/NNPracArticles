# PubMed Article Usefulness Predictor

This project implements a binary neural network classifier to predict the usefulness of PubMed articles based on their relevance to machine learning applications in cancer research. It combines web scraping, language model embeddings, and a custom-built neural network to classify articles as "useful" (1) or "not useful" (0). The project draws inspiration from *Neural Networks from Scratch in Python* by Harrison Kinsley and Daniel Kukieła, applying neural network concepts to enhance research workflow efficiency through large language model (LLM) integration. The project is approximately 95% complete, with ongoing improvements in dataset size and model performance.

For implementation details, see `CompleteBiArticlePredictor.ipynb`.

## Project Overview

The goal is to automate the classification of PubMed articles as useful or not based on a user-defined prompt, leveraging LLMs for labeling and embeddings, and a neural network for binary classification. The workflow includes:

1. **Scraping PubMed**: Fetch article metadata (title, abstract) using the PubMed API.
2. **Summarization and Labeling**: Use the Llama3 model via Ollama to summarize articles and assign binary labels (1 for useful, 0 for not useful) based on a prompt tailored to machine learning in cancer research.
3. **Embedding Generation**: Convert article summaries into high-dimensional embeddings using the `nomic-embed-text` model.
4. **Neural Network Training**: Train a custom neural network on these embeddings to predict article usefulness.
5. **Evaluation and Visualization**: Assess model performance with loss and accuracy metrics, visualized over training epochs.

The model streamlines research by identifying practically valuable articles (e.g., those describing machine learning techniques for cancer diagnosis or treatment) while filtering out less relevant ones (e.g., reviews or purely theoretical studies).
