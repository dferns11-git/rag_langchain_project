# rag_langchain_project
A Retrieval Augmented Generation (RAG) system leveraging LangChain and Chroma DB for efficient querying of Markdown documents, enhanced by OpenAI embeddings for accurate and context-aware responses.

## Features

- **Environment Setup**: 
  - Isolated virtual environment for dependency management.
  
- **Document Loading**: 
  - Utilizes LangChain's `TextLoader` for document ingestion, simplifying the process and ensuring compatibility.

- **Database Management**: 
  - Builds and manages a Chroma DB to store vector embeddings, ensuring efficient data retrieval.

- **Embedding Integration**: 
  - Leverages OpenAI's embedding models via Chroma DB for enhanced semantic search capabilities.

- **Query Implementation**: 
  - Supports user queries with contextually relevant and accurate document retrieval.

## Installation

### Prerequisites
- Python 3.8+
- OpenAI API Key
- Chroma DB library
- LangChain library

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/rag-system.git
   cd rag-system
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Add your OpenAI API key in a `.env` file:
   ```env
   OPENAI_API_KEY=your_openai_api_key
   ```

5. Run the application:
   ```bash
   python app.py
   ```

## Usage

1. Place your Markdown documents in the `documents/` folder.
2. The system will process these documents and create a Chroma DB with embeddings.
3. Use the command-line interface or API to query the system for contextually relevant responses.

## Project Workflow

1. **Document Ingestion**: Markdown files are loaded using `TextLoader`.
2. **Embedding Generation**: OpenAI embeddings are generated for the loaded documents.
3. **Database Creation**: Chroma DB stores the generated embeddings for efficient querying.
4. **Query Execution**: User input queries are processed, and the most relevant documents are retrieved based on semantic similarity.

## Challenges and Solutions

- **Document Loading**: LangChain's `DirectoryLoader` encountered compatibility issues due to the `libmagic` dependency. Replacing it with `TextLoader` ensured a smoother workflow.
- **Embedding Storage**: Chroma DB's integration streamlined storage and retrieval, minimizing complexity while maximizing efficiency.

## Future Enhancements

- Implementing pre-processing techniques like summarization and keyword extraction to improve retrieval accuracy.
- Adding support for querying multimodal data (e.g., PDFs and images).
- Exploring advanced ranking algorithms to prioritize responses.

## Contributing

Contributions are welcome! Feel free to fork the repository, submit issues, or create pull requests.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

### Acknowledgments
- [LangChain Documentation](https://www.langchain.com)
- [Chroma DB Documentation](https://docs.trychroma.com)
- [OpenAI API Documentation](https://platform.openai.com/docs)

