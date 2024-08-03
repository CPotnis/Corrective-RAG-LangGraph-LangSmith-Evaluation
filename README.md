# Corrective RAG: LangGraph, LangSmith Evaluation (Llama 3.1)

## Project Overview

This project implements a Corrective Retrieval-Augmented Generation (RAG) system using LangGraph and evaluates its performance with LangSmith. The system aims to improve the quality of responses by incorporating web search when necessary and grading the relevance of retrieved documents.

## Features

- Document loading and preprocessing
- Vector store creation for efficient retrieval
- Llama 3.1 integration via Ollama for language modeling
- Web search capability using Tavily
- Custom graph-based RAG pipeline
- LangSmith integration for evaluation

## Prerequisites

- Anaconda or Miniconda
- Ollama with Llama 3.1 model installed
- API keys for OpenAI, Tavily, and LangChain

## Installation

1. Clone the repository:

```
git clone https://github.com/CPotnis/corrective-rag.git
cd corrective-rag
```
2. Create and activate a conda environment:
```
conda env create -f environment.yml
conda activate corrective-rag
```


3. Set up your environment variables by creating a `.env` file in the project root:
```
OPENAI_API_KEY=your_openai_api_key
TAVILY_API_KEY=your_tavily_api_key
LANGCHAIN_API_KEY=your_langchain_api_key
```
## Running the Notebook

1. Start Jupyter Notebook:
```
jupyter notebook
```
2. Open the `corrective_rag.ipynb` notebook.

3. Run the cells in order, following the comments and explanations provided.

## Notebook Structure

The notebook is structured into the following sections:

1. Library Imports and Environment Setup
2. Data Loading and Preprocessing
3. Model Initialization and Configuration
4. Corrective RAG Pipeline Implementation
5. Example Usage of the Pipeline
6. LangSmith Evaluation Setup
7. Main Execution

## Key Components

- `load_and_process_data()`: Loads and preprocesses the PDF document.
- `initialize_models()`: Sets up the Llama 3.1 model, RAG chain, and retrieval grader.
- `build_graph()`: Constructs the LangGraph for the Corrective RAG pipeline.
- `predict_custom_agent_answer()`: Runs a query through the RAG pipeline.
- `setup_langsmith_evaluation()`: Prepares the LangSmith evaluation dataset.
- `run_evaluation()`: Executes the LangSmith evaluation.

## Customization

- To use a different PDF, update the `file_path` variable in the notebook.
- Adjust the `chunk_size` and `chunk_overlap` in the text splitter for different document segmentation.
- Modify the prompts in `initialize_models()` to change the system's behavior.

## Troubleshooting

- Ensure Ollama is running and the Llama 3.1 model is available.
- Check that all API keys are correctly set in the `.env` file.
- If you encounter memory issues, try reducing the `chunk_size` or processing a smaller document.

## Contributing

Contributions to improve the Corrective RAG system are welcome. Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add some feature'`)
5. Push to the branch (`git push origin feature/your-feature`)
6. Create a new Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- LangChain for providing the framework for building LLM applications
- Ollama for the Llama 3.1 model integration
- Tavily for web search capabilities
- LangSmith for evaluation tools

For any questions or issues, please open an issue in the GitHub repository.