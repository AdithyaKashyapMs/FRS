# Food Recommendation Search (FRS)

A Python-based food recommendation and search toolkit that combines semantic similarity search with a conversational RAG chatbot experience.

## Project Overview

This repository provides a food search system based on a structured food dataset and vector similarity search using ChromaDB. It includes three main modes:

- **Interactive Search**: A CLI chatbot for direct food queries and recommendations.
- **Advanced Search**: A CLI interface with cuisine, calorie, and combined filter support.
- **Enhanced RAG Chatbot**: A retrieval-augmented generation system using IBM watsonx.ai Granite for conversational food recommendations.
- **System Comparison**: A demo comparing the three search approaches.

## Repository Structure

- `FRS/shared_functions.py` - shared utilities for loading the dataset, creating ChromaDB collections, embedding food records, and performing similarity searches.
- `FRS/interactive_search.py` - interactive CLI food search chatbot.
- `FRS/advanced_search.py` - advanced search demo with filter options and search demonstrations.
- `FRS/enhanced_rag_chatbot.py` - enhanced RAG-powered chatbot with IBM watsonx.ai integration.
- `FRS/system__comparison.py` - comparison script for interactive, advanced, and RAG workflows.
- `FRS/FoodDataSet.json` - food dataset used by all systems.

## Requirements

- Python 3.8+
- `chromadb`
- `ibm-watsonx-ai`
- `numpy`

Optional but recommended:
- `sentence-transformers` (used by the ChromaDB sentence embedding function)

## Installation

```bash
python -m pip install chromadb ibm-watsonx-ai numpy sentence-transformers
```

> Note: The RAG chatbot requires valid IBM watsonx.ai credentials and may require additional environment configuration for the `ibm-watsonx-ai` SDK.

## Usage

From the repository root, run one of the scripts below:

### 1. Interactive Search

```bash
python FRS/interactive_search.py
```

Use natural language queries to search for food items and view recommendations.

### 2. Advanced Search

```bash
python FRS/advanced_search.py


Explore advanced search modes:
- Basic similarity search
- Cuisine-filtered search
- Calorie-filtered search
- Combined filters
- Demonstration mode

### 3. Enhanced RAG Chatbot

```bash
python FRS/enhanced_rag_chatbot.py
```

This mode retrieves relevant food items from the dataset and uses IBM Granite to generate conversational responses.

### 4. System Comparison

```bash
python FRS/system__comparison.py
```

Run a benchmark and compare the performance and output style of the three search systems.

## Notes

- The dataset is loaded from `FRS/FoodDataSet.json`.
- ChromaDB uses the `all-MiniLM-L6-v2` embedding model to build similarity search vectors.
- The RAG chatbot code includes a placeholder IBM watsonx.ai configuration, so update `my_credentials`, `project_id`, and related settings as needed.

## License

This repository does not include an explicit license file. Use and modify the code according to your own requirements.


