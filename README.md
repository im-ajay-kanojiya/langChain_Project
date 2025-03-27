# PDF Analysis Assignment

## Project Overview

This project is designed to process and analyze text content within PDF documents using AI. It leverages tools like **LangChain**, **Google Generative AI**, and **FAISS** for text extraction, vector storage, and embedding-based search functionalities. The primary goal is to provide users with an interface that allows uploading a PDF, extracting its contents, and then querying the text with natural language questions.

## Key Features

- **PDF Text Extraction**: Extracts text from each page in a PDF and consolidates it.
- **Text Chunking**: Splits extracted text into manageable chunks for processing by language models.
- **Embedding Generation**: Creates embeddings for text chunks, enabling semantic search.
- **Question Answering (Q&A)**: Provides a natural language Q&A interface using Google Generative AI’s model to retrieve answers from PDF content.

## Requirements

To run this project, you’ll need the following Python libraries:

- `google-generativeai`
- `faiss-cpu`
- `langchain`
- `PyPDF2`

Install the dependencies using:
```bash
pip install -U -q "google-generativeai>=0.7.2" faiss-cpu langchain PyPDF2
```

## Usage Guide

### Steps to Analyze a PDF

1. **Upload a PDF**: The notebook includes a widget to upload a PDF document.
2. **Text Extraction**: Automatically reads the PDF, displaying the number of pages and extracted text.
3. **Text Chunking**: Text is divided into smaller, overlapping chunks for efficient processing.
4. **Embedding Creation**: Each text chunk is converted into vector embeddings for searchability.
5. **Question Answering**: Use the embedded Q&A chain to ask questions about the document content.

### Example Commands

- Generate embeddings:
  ```python
  document_search = FAISS.from_texts(texts, embeddings)
  ```
- Ask a question about the PDF content:
  ```python
  response = chain.run("What is the main topic of the document?")
  print(response)
  ```

## File Structure

- `FluidAI_Assignment.ipynb`: The main notebook file containing code for PDF processing and Q&A.
- `data/`: Folder for storing PDF files (if included for reference).

## Future Improvements

- **Error Handling**: Implement checks for various PDF formats and page layouts.
- **Enhanced Q&A Performance**: Tune model parameters or try alternative models.
- **Multi-PDF Processing**: Enable analysis of multiple PDFs in one session.

## Troubleshooting

- Ensure that the API key is set up correctly if you encounter authorization errors.
- If embeddings generation fails, check the compatibility of FAISS and the embeddings model.

--- 

This README template should provide a clear understanding of the notebook’s functionality and help users get started quickly. Let me know if you need further refinement!
