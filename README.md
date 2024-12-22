# Wikipedia Q&A Bot

Welcome to the **Wikipedia Q&A Bot**! This interactive Jupyter Notebook allows users to load any Wikipedia page and ask questions about its content. The bot utilizes LangChain and Hugging Face's Sentence Transformers to provide accurate answers based on the loaded text.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Contributing](#contributing)
- [License](#license)

## Features

- Load any Wikipedia page by title.
- Ask questions about the content of the loaded page.
- Get relevant answers based on the text extracted from Wikipedia.
- Built with Python for easy customization and extension.

## Installation

To run this project locally, follow these steps:

1. **Clone the repository**:
	```bash
	git clone https://github.com/RoystonDAlmeida/wikipedia-qa-bot.git
	cd wikipedia-qa-bot
	```

2. **Install the required packages**:
Make sure you have Python installed (preferably Python 3.7 or higher). Then, install the necessary libraries. The libraries are specified in the first cell in the notebook.

- Alternatively, you can install the packages directly:
	```bash
	pip install wikipedia-api langchain langchain-huggingface chromadb
	```

3. **Install Jupyter Notebook** (if not already installed):
You can install Jupyter Notebook using pip:
	```bash
	pip install notebook
	```

## Usage

1. **Launch Jupyter Notebook**:
In your terminal, navigate to the project directory and run:
	```bash
	jupyter notebook
	```

2. **Open the Notebook**:
In your web browser, navigate to `http://localhost:8888` (or follow the link provided in your terminal). Open the `Wikipedia_QA_Bot.ipynb` notebook.

3. **Run the Notebook Cells**:
- Follow the instructions in each cell to load a Wikipedia page by entering a valid title (e.g., "Python (programming language)").
- Execute the cells sequentially to load the page and set up the Q&A bot.
- Ask questions related to its content by running the appropriate cells.

## How It Works

1. **Loading Wikipedia Pages**: The bot uses the `wikipedia-api` library to fetch content from Wikipedia based on user input.

2. **Text Processing**: The text is split into chunks using LangChain's `CharacterTextSplitter` for efficient processing.

3. **Embeddings**: The `HuggingFaceEmbeddings` class from `langchain-huggingface` creates embeddings for each chunk of text, enabling semantic search.

4. **Querying**: When a user asks a question, the bot performs a similarity search against the embeddings to find relevant answers.

## Contributing

We welcome contributions! To contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes and commit them (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

Please ensure that your code adheres to our coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Thank you for checking out our Wikipedia Q&A Bot! We hope you find it useful and engaging. If you have any questions or feedback, feel free to reach out!
