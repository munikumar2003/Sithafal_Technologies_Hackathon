# Sithafal_Technologies_Hackathon
# PDF Data Extraction and Analysis

This project extracts and processes structured data (tables) and semi-structured data (graphs, charts) from PDF files using a combination of libraries like **Camelot** for table extraction and **PyMuPDF** (fitz) for graph detection. The data is then converted into a structured JSON format for further analysis or processing.

## Project Overview

This repository provides a solution for extracting tables and graphs from PDFs and converting them into a JSON structure. This is useful for scenarios where PDF documents contain key data such as tables and graphs that need to be analyzed or processed further.

### Key Features
- Extracts tables from PDF files using **Camelot**.
- Detects and extracts graphs (you can integrate your own graph extraction method).
- Converts the extracted data into a structured JSON format for easy use.
  
## Requirements

You can run this project on Google Colab or your local machine.

### Installation

To get started, you’ll need the following dependencies:

1. **Camelot** for table extraction.
2. **PyMuPDF** (fitz) for working with PDFs.
3. **pytesseract** for OCR-based graph extraction (if needed).

### Installation via pip

```bash
pip install camelot-py[cv]
pip install pymupdf
pip install pytesseract
```
# Chat with Website Using RAG Pipeline

## Overview

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline that enables users to interact with structured and unstructured data extracted from websites. The system crawls, scrapes, and stores website content, converts it into embeddings, and stores the embeddings in a vector database for efficient retrieval. Users can query the system for information, and the system will generate context-rich and accurate responses using a selected language model (LLM).

## Functional Requirements

### 1. Data Ingestion
- **Input**: URLs or a list of websites to crawl/scrape.
- **Process**:
  - **Crawl and Scrape**: Crawl and scrape content from target websites.
  - **Data Extraction**: Extract key data fields, metadata, and textual content.
  - **Segmentation**: Segment content into smaller chunks for better granularity and more efficient processing.
  - **Embedding Generation**: Convert content chunks into vector embeddings using a pre-trained embedding model.
  - **Vector Database Storage**: Store embeddings in a vector database along with metadata for efficient retrieval.

### 2. Query Handling
- **Input**: User's natural language query.
- **Process**:
  - **Query Embedding**: Convert the user's query into vector embeddings using the same embedding model used for content.
  - **Similarity Search**: Perform a similarity search in the vector database to retrieve the most relevant content chunks.
  - **Response Generation**: Pass the retrieved chunks to the LLM along with context to generate a detailed response.

### 3. Response Generation
- **Input**: Relevant information retrieved from the vector database and the user's query.
- **Process**:
  - **LLM Response**: Use the LLM with retrieval-augmented prompts to generate responses, incorporating relevant chunks directly into the response to ensure accuracy and contextuality.
  - **Factuality Assurance**: Ensure that the generated response contains exact values and data retrieved from the website's content.

## Example Website Links

This system supports crawling and scraping of websites for the following examples:

- [University of Chicago](https://www.uchicago.edu/)
- [University of Washington](https://www.washington.edu/)
- [Stanford University](https://www.stanford.edu/)
- [University of North Dakota](https://und.edu/)

## Project Setup

### Prerequisites

1. Python 3.8 or higher
2. Required Python libraries:
   - `requests` (for crawling)
   - `beautifulsoup4` (for scraping)
   - `transformers` (for language model and embeddings)
   - `faiss` or `chromadb` (for vector database storage)
   - `numpy` (for numerical operations)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/rag-pipeline.git
   cd rag-pipeline
Install the required dependencies:

```bash
pip install -r requirements.txt
Set up the vector database (e.g., FAISS or Chroma). Follow the specific database setup instructions from the respective documentation.
```
**Configuration**
Set the websites to be crawled by modifying the websites.txt or through the function parameters.
Configure your vector database settings in the config.py file.
Running the System
Crawl and scrape website content:

```bash
python crawl_and_scrape.py
Query the system:
```
```bash
python query_system.py "What is the university's research focus?"
Get response: The system will generate a detailed response based on the relevant content retrieved from the vector database.
```
**Usage Example
Crawling & Scraping**
You can specify the list of URLs to scrape in a file or directly pass the URLs to the crawling function. The system will scrape the web pages and convert the relevant textual content into embeddings.
**Querying**
Once the data is ingested into the system and stored in the vector database, you can query the system using a natural language question. The system will retrieve the relevant chunks of data and pass them to the language model to generate a context-rich response.

**Example query:**
**Input:** "What are the top departments at the University of Chicago?"
**Response:** The system will return a response with information such as "The University of Chicago has strong departments in economics, law, and business."

**Future Enhancements**
Expand Support for More Websites: Extend the crawling support to other websites.
Improve Embedding Accuracy: Tune the embedding model for better context representation.
Customizable Query Handling: Allow users to add their own question-answering logic.
Advanced Data Processing: Improve the segmentation and metadata extraction for more granular content retrieval.
License
This project is licensed under the MIT License - see the LICENSE file for details.

**Acknowledgments**
The RAG architecture is based on techniques introduced by Facebook AI Research.
Embedding models are sourced from Hugging Face.
Contact
For further inquiries or contributions, please contact [munikumarchemuru2003@gmail.com].
### Key Sections:
- **Overview**: Describes the purpose and function of the RAG pipeline.
- **Functional Requirements**: Detailed breakdown of the ingestion, query handling, and response generation processes.
- **Installation**: Instructions on setting up the project and dependencies.
- **Configuration**: Customizing the crawling and scraping sources.
- **Usage Example**: How to use the system after setup.
- **Future Enhancements**: Ideas for future improvements to the system.
- **License**: Information about the project's licensing.
- **Acknowledgments**: Credit to relevant resources or tools used.
- **Contact**: How to reach the project maintainer.

