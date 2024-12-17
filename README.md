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
