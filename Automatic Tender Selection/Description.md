# Tender and Bid Evaluation System

## Project Overview

This project involves creating a system to extract and analyze data from tender and bid PDFs. The goal is to evaluate bid submissions based on the specifications, requirements, and criteria outlined in the tender document and to identify the best bid that meets all requirements.

## Project Code

You can find the complete project code at the following link:

[**Project Code Repository**](https://github.com/yourusername/your-repository-name)

## Project Components

### 1. **PDF Text Extraction**
   - **Purpose**: Extract text data from tender and bid PDF files.
   - **Libraries Used**: `PyPDF2` for PDF text extraction.
   - **Input**: Path to tender PDF and multiple bid PDFs.
   - **Output**: Structured text data from the PDFs.

### 2. **Data Parsing and Processing**
   - **Purpose**: Parse the extracted text data to identify and extract relevant information such as tender details, bid specifications, price, delivery time, etc.
   - **Method**: Regular expressions and string manipulation to isolate sections and details.

### 3. **Evaluation Logic**
   - **Purpose**: Evaluate bids based on the tender criteria, such as price, delivery time, and warranty.
   - **Logic**: Compare bid details against the tender's requirements and score each bid.

### 4. **Result Presentation**
   - **Purpose**: Display a summary table of all bids and highlight the best bid based on evaluation criteria.
   - **Libraries Used**: `pandas` for data structuring and display.
   - **Output**: A formatted table with bid details and the best bid highlighted.

## Project Features

- **PDF Processing**: Efficient extraction of text from both tender and bid PDF files.
- **Custom Evaluation**: Tailored logic to evaluate bids based on multiple criteria, such as price and compliance with specifications.
- **Tabular Display**: Visual representation of bid data with an emphasis on the best bid for quick decision-making.
