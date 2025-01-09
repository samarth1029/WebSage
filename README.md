# WebSage

WebSage is a powerful Retrieval-Augmented Generation (RAG) system that combines advanced web scraping with generative AI to answer questions from any given website.

This repository implements a Retrieval-Augmented Generation (RAG) system using Hugging Face models and LangChain. The system combines document retrieval with generative AI to answer questions based on content scraped from a given website URL.

## Features
- **LLM Used**: The LLM used for RAG in this repository is available at [Baymax-Gemma-2-9B GitHub Repository](https://github.com/samarth1029/baymax-gemma-2-9B) and on [Hugging Face](https://huggingface.co/samarth1029/Gemma-2-2b-baymax).
- **Web Scraping**: Extract content from a given website.
- **Chunk Splitting**: Split large text into manageable chunks for efficient processing.
- **FAISS Indexing**: Use FAISS for efficient similarity search and retrieval.
- **Generative AI**: Integrate Hugging Face models like `samarth1029/Gemma-2-2b-baymax` for question answering.
- **Interactive UI**: Use widgets for secure Hugging Face login, URL input, and question submission.

## Setup

### Prerequisites
- Python 3.7+
- Install required libraries:
  ```bash
  pip install requests beautifulsoup4 langchain transformers huggingface_hub faiss-cpu ipywidgets
  ```

### Clone the Repository
```bash
git clone https://github.com/<your-username>/WebSage.git
cd WebSage
```

### Hugging Face Authentication
Use your Hugging Face token for model access:
1. Obtain a token from [Hugging Face](https://huggingface.co/settings/tokens).
2. Enter the token when prompted in the notebook UI.

## Usage

1. Open the provided notebook in Kaggle, Colab, or Jupyter Notebook.
2. Run the cells to:
  - Login to Hugging Face.
  - Input the website URL and your question.
3. The system will:
  - Scrape the website content.
  - Create a FAISS index for document retrieval.
  - Use the Hugging Face model to generate an answer.

## Example
- **Input URL**: `https://example.com`
- **Input Question**: `What is the main topic of the website?`
- **Output**:
  ```
  Answer: The website discusses examples and best practices for web development.
  ```

## File Structure
- `notebooks/baymax_RAG.ipynb`: Source code for the RAG system implementation in Jupyter Notebook.
- `docs/GenAI_RAG_task - Colab.pdf`: A sample run of the RAG system exported and saved as a PDF document.
- `README.md`: Documentation and instructions.
- `notebooks/baymax_RAG.ipynb`: Source code for the RAG system implementation in Jupyter Notebook.
- `README.md`: Documentation and instructions.

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
