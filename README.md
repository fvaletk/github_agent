GitHub Issues Summarizer
========================

Overview
--------

This project utilizes the Retriever-Generator (RAG) architecture to intelligently summarize issues from a GitHub repository. Leveraging the power of AstraDB and LangChain's AI capabilities, this application provides a seamless way to extract, store, and analyze GitHub issues, enabling users to quickly understand key topics and ongoing discussions in a repository.

Features
--------

-   **Issue Retrieval**: Fetches issues from specified GitHub repositories using the GitHub API.
-   **Data Storage**: Utilizes AstraDB to store and manage retrieved issue data, ensuring scalable and efficient data handling.
-   **Intelligent Summarization**: Employs LangChain's advanced AI to generate summaries of issues, helping maintainers and contributors grasp the essence of discussions without delving into every single thread.
-   **Vector-based Search**: Supports searching through issues using semantic search techniques to find the most relevant discussions based on query matching.

How It Works
------------

1.  **Fetching Issues**: The application first fetches issues from a designated GitHub repository.
2.  **Data Storage**: Issues are then stored in AstraDB, with each issue vectorized for efficient retrieval.
3.  **Summarization**: Upon request, the system retrieves relevant issues based on input queries and uses an AI model to generate concise summaries.
4.  **Query Interface**: Users can input queries related to specific issues, and the system will provide summaries of the top relevant issues.

Getting Started
---------------

### Prerequisites

-   Python 3.8+
-   Pipenv or virtualenv
-   Access to AstraDB (DataStax)
-   OpenAI API key

### Installation

1.  Clone the repository:

```bash
      git clone https://github.com/yourusername/github-issues-summarizer.git
```

3.  Navigate to the project directory:

```bash
      cd github-issues-summarizer
```

4.  Install dependencies:

```bash
      pipenv install  # or use pip install -r requirements.txt
```

### Configuration

Create a `.env` file in the project root and populate it with your credentials:

```
ASTRA_DB_API_ENDPOINT=https://api-astra.datastax.com/
ASTRA_DB_APPLICATION_TOKEN=Your_AstraDB_Token
ASTRA_DB_KEYSPACE=Your_Desired_Keyspace
OPENAI_API_KEY=Your_OpenAI_API_Key
```

### Usage

Run the application:


```bash
  pipenv run python main.py
```


Follow the prompts in the console to fetch and summarize issues.

Contributing
------------

Contributions are welcome! Feel free to fork the project and submit pull requests. If you have ideas for features or notice any issues, please open an issue in the repository.

License
-------

Distributed under the MIT License. See `LICENSE` for more information.
