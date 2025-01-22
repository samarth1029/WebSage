# Web Sage - RAG-based Question Answering with Voice Input
Web Sage is a Retrieval-Augmented Generation (RAG) system that answers user queries based on content scraped from a provided URL. The system supports text and voice input, processes the input using a large language model (LLM), and provides both text and audio responses using PyTorch-based text-to-speech (TTS).

## Sample Run
- A sample screen recording for the text-to-text output can be found [here]( https://www.loom.com/share/2f1b49ed515f489ab201b9c14e64c6a8?sid=c96ff6ce-43a6-41c6-8e9a-28856df5fc6b).
- A sample screen recording for the speech-to-speech output can be found [here]( https://www.loom.com/share/0a1fc68e81574f50a88185d6936fb83b?sid=6a4e4d79-67ad-466c-b316-5ff01cb1c714).

## Features
- **Web Scraping:** Automatically extracts text content from a given URL.
- **Voice Input:** Allows users to provide queries using an uploaded audio file.
- **Retrieval-Augmented Generation (RAG):** Uses FAISS for efficient document retrieval and a transformer-based LLM for response generation.
- **Text-to-Speech (TTS):** Converts the generated text answer to an audio output.
- **Interactive UI:** Provides a user-friendly interface using `ipywidgets` in Jupyter/Colab notebooks.

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
  ![Sample](https://raw.githubusercontent.com/samarth1029/WebSage/main/results/sample.jpg)


## File Structure
- `notebooks/Fargo_RAG_Multimodal.ipynb`: Source code for the Multimodal RAG system implementation that takes in voice input and generates audio response in Jupyter Notebook.
- `notebooks/Fargo_finetune.ipynb`: Source code for PEFT on gemma-2b base model on financial dataset
- `results/Fargo_RAG_Multimodal.ipynb - Colab.pdf`: A sample run of the Multimodal RAG system exported and saved as a PDF document.
- `README.md`: Documentation and instructions.

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
