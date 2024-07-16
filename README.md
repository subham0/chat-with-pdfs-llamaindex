# Chat with Financial Documents

This project demonstrates how to create a Question and Answer (Q&A) system using PDFs containing text, images, and tables. The system leverages `llama-parse` with GPT-4o for parsing the PDF and querying the extracted content using a Retrieval-Augmented Generation (RAG) pipeline.

## Project Structure

The project contains the following files:
1. **Chat with Financial Document.ipynb** - A Jupyter notebook that contains the entire code and walks through the entire process of setting up the Q&A system.
2. **requirements.txt** - A text file that lists all the Python packages required to run the code.
3. **TSLA-Q3-2023-Update-3.pdf** - The PDF file containing the financial document that will be used for the Q&A.

## Setup Instructions

### Prerequisites

Ensure you have Python installed on your system. This project was developed and tested with Python 3.11.

### Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/subham0/chat-with-pdfs-llamaindex.git
    cd chat-with-pdfs-llamaindex
    ```

2. **Create a virtual environment**:
    ```bash
    python -m venv venv
    source venv/bin/activate   # On Windows use `venv\Scripts\activate`
    ```

3. **Install the required packages**:
    ```bash
    pip install -r requirements.txt
    ```

### Running the Jupyter Notebook

1. **Start Jupyter Notebook**:
    ```bash
    jupyter notebook
    ```

2. **Open and Run**:
    - Navigate to the `Chat with Financial Document.ipynb` file and open it.
    - Run each cell sequentially to execute the code and follow the step-by-step instructions provided within the notebook.

## Project Overview

### 1. PDF Parsing with `llama-parse`

The project utilizes `llama-parse` which internally uses GPT-4o, a fully multimodal model by OpenAI. This model, released in May 2024, significantly improves vision and audio capabilities, making it ideal for document parsing. Each page of the PDF is treated as an image and processed for content extraction.

### 2. Content Vectorization

After parsing the PDF, the extracted content is stored in `llama-index`'s default in-memory vector store. The embedding model used for vectorizing the content is OpenAI's `text-embedding-ada002` model.

### 3. Retrieval-Augmented Generation (RAG) Pipeline

Once the content is vectorized and indexed, a RAG pipeline is created. This pipeline is used to query the PDF and provide answers based on the embedded content.

## How to Use

### Querying the PDF

After running the notebook, you can interact with the Q&A system by inputting your questions related to the content of the `TSLA-Q3-2023-Update-3.pdf` file. The system will retrieve relevant information from the embedded content and generate a response.

## Contact

For any questions or support, please contact - 

- **Name**: Subham Gupta
- **Email**: subhuwin@gmail.com
- **GitHub**: [subham0](https://github.com/subham0)

