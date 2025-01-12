# WebSage

WebSage is a Retrieval-Augmented Generation (RAG) system that combines web scraping with generative AI to answer questions from any given website.

This repository implements a Retrieval-Augmented Generation (RAG) system using Hugging Face models and LangChain. The system combines document retrieval with generative AI to answer questions based on content scraped from a given website URL.

## Sample Run
A sample screen recording for the output can be found [here]( https://www.loom.com/share/2f1b49ed515f489ab201b9c14e64c6a8?sid=c96ff6ce-43a6-41c6-8e9a-28856df5fc6b).

## Features
- **LLM Used**: The LLM used for RAG in this repository was fine-tuned using a specialized [Banking Dataset](https://huggingface.co/datasets/AmjadKha/BankingDataset). The finetuning process is documented in detail at [Gemma-2b-fargo-finetune](https://github.com/samarth1029/WebSage/blob/main/notebooks/Fargo_Finetune.ipynb). The resulting model is publicly available on [Hugging Face](https://huggingface.co/shriasannuthi/gemma-2b-fargo).
- **Web Scraping**: Extract content from a given website.
- **Chunk Splitting**: Split large text into manageable chunks for efficient processing.
- **FAISS Indexing**: Use FAISS for efficient similarity search and retrieval.
- **Generative AI**: Integrate Hugging Face models like `shriasannuthi/gemma-2b-fargo` for question answering.
- **Interactive UI**: Use widgets for secure Hugging Face login, URL input, and question submission.

## Setup

### Prerequisites
- Python 3.7+
- Install required libraries:
  ```bash
  pip install requests beautifulsoup4 langchain transformers huggingface_hub faiss-cpu ipywidgets
  ```
- Access to these repositories are to be raised:
  - [shriasannuthi/gemma-2b-fargo](https://huggingface.co/shriasannuthi/gemma-2b-fargo)
  - [google/gemma-2-2b-it](https://huggingface.co/google/gemma-2-2b-it)

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
  ![Sample](https://raw.githubusercontent.com/samarth1029/WebSage/main/docs/sample.jpg)


## File Structure
- `notebooks/Fargo_RAG.ipynb`: Source code for the RAG system implementation in Jupyter Notebook.
- `notebooks/Fargo_finetune.ipynb`: Source code for PEFT on gemma-2b base model on financial dataset
- `docs/Fargo_RAG.ipynb - Colab.pdf`: A sample run of the RAG system exported and saved as a PDF document.
- `README.md`: Documentation and instructions.

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
