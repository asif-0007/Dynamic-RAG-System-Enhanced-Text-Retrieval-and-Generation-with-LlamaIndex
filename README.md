# Dynamic RAG System: Enhanced Text Retrieval and Generation with LlamaIndex

## Overview
This project implements a **Retrieval-Augmented Generation (RAG)** system, combining advanced information retrieval with generative language models to create an efficient and scalable solution for extracting, processing, and retrieving information from various sources. The system utilizes cutting-edge technologies and frameworks to achieve high performance in text extraction, retrieval, and response generation.

---

## Features
- **Efficient Data Retrieval**: Leverages FAISS for fast and accurate retrieval of relevant documents.
- **Versatile Text Extraction**: Supports content scraping from multiple sources, including images and tables.
- **Scalable Architecture**: Built on LlamaIndex, providing ease of integration and scalability.
- **Interactive Bot Interface**: Allows user-friendly interactions through a Gradio-powered chatbot.

---

## Technology Stack

### Web Scraping
- **DuckDuckGo**: Used as the search engine for gathering web pages.
- **OpenCV and Tesseract**: Extracts text from images found on web pages.
- **Table Extraction**: Processes data from tables on web pages and converts them into structured documents.

### Document Processing
- Converts scraped and extracted content into documents.
- Filters out empty or irrelevant documents to retain only meaningful information.

### Language Model
- **Hugging Face**: Utilizes the **Meta-Llama-3.1-8B-Instruct model** as the primary large language model (LLM).

### Embedding Model
- Uses **sentence-transformers/all-MiniLM-L6-v2** to generate embeddings for documents, enabling semantic understanding and retrieval.

### Vector Database
- **FAISS**: A high-performance vector indexing library used to optimize search and retrieval operations, replacing the default VectorStoreIndex in LlamaIndex.

### Bot Interface
- **Gradio**: Provides an interactive interface for users to interact with the system for Q&A, content retrieval, and more.

---

## System Workflow

1. **Data Acquisition**
   - Web pages are scraped using DuckDuckGo as the search engine.
   - Text content, including text from images (via OpenCV and Tesseract) and tables, is extracted for further processing.

2. **Document Preparation**
   - Extracted data is processed into structured documents.
   - Empty or irrelevant content is filtered out, retaining only meaningful documents.

3. **Embedding and Indexing**
   - Document embeddings are generated using **sentence-transformers/all-MiniLM-L6-v2**.
   - Embeddings are indexed in **FAISS** for optimized retrieval.

4. **RAG Pipeline**
   - When a user queries the system, relevant documents are retrieved using FAISS.
   - Retrieved content is fed into the **Meta-Llama-3.1-8B-Instruct model**, augmenting the generation process with contextual data.

5. **User Interaction**
   - The system outputs generated responses via a Gradio-based chatbot interface, enabling real-time Q&A and content exploration.

---

## Benefits
- **Performance**: Combines powerful embedding and indexing techniques for fast and accurate document retrieval.
- **Flexibility**: Handles diverse data types (text, images, tables) seamlessly.
- **Scalability**: Built on LlamaIndex, ensuring robust performance across varying workloads.
- **User Experience**: Simplifies interaction with a clean, intuitive Gradio interface.

## Usage
1. Enter a query in the Gradio chatbot interface.
2. The system retrieves relevant documents using FAISS.
3. The retrieved documents augment the generation process of the Llama model.
4. View the generated response in real time.

---

## Future Enhancements
- **Additional Data Sources**: Expand support for more diverse data sources, such as PDFs and APIs.
- **Model Upgrades**: Integrate larger and more advanced LLMs for improved response quality.
- **Enhanced UI**: Develop a more interactive and feature-rich user interface.



