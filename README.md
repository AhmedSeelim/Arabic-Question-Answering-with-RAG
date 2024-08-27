# Arabic-RAG-Powered-QA-Assistant

## Overview
The "Arabic-RAG-Powered-QA-Assistant" project is focused on developing an advanced Question Answering (QA) system designed specifically for Arabic language queries. The system employs Retrieval-Augmented Generation (RAG) techniques to provide accurate, contextually relevant answers by retrieving and generating responses based on a knowledge base.

## Features
- **RAG Implementation:** Combines document retrieval and generation to improve the quality of answers.
- **Arabic Language Support:** Tailored to process and understand Arabic queries effectively.
- **SANAD Dataset:** Utilizes the SANAD dataset for building a robust Arabic knowledge base.
- **Simple Interface:** A user-friendly graphical interface to input questions and receive detailed answers.


## Usage

To use the Arabic-RAG-Powered-QA-Assistant, follow these steps:

1. **Prepare the Dataset:**
   - Download the SANAD dataset and place it in the `data/` directory.

2. **Generate Document Embeddings:**
   - Use the SentenceTransformer model to generate embeddings for the documents in your knowledge base. This step is essential for the retrieval process:
     ```python
     from sentence_transformers import SentenceTransformer

     model = SentenceTransformer('sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2')
     embeddings = model.encode(documents)
     ```

3. **Start the QA System:**
   - Run the QA system by inputting your questions through the interface:
     ```python
     from src.qa_system import process_question

     question = "Your question in Arabic"
     answer = process_question(question)
     print(answer)
     ```

4. **Use the Graphical Interface:**
   - Launch the Gradio interface to interact with the QA assistant in a user-friendly way



## Requirements

To run the Arabic-RAG-Powered-QA-Assistant, you need the following software and libraries:

- **Python 3.x:** Make sure Python 3.x is installed on your system.
- **Python Libraries:**
  - `SentenceTransformers`
  - `LangChain`
  - `PyTorch`
  - `Chroma`
  - `Gradio`



