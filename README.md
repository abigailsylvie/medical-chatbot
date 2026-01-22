# Medibot

Medibot is a simple medical chatbot built using a Retrieval-Augmented Generation (RAG) approach. It allows users to ask questions about medical documents and receive answers grounded in the provided data.

## Project Overview

The system processes medical documents, splits them into smaller text chunks, converts them into vector embeddings, and stores them in a vector database. When a user asks a question, the most relevant chunks are retrieved and passed to a language model to generate an informed response.

## Tech Stack

* Python 3.10
* LangChain
* OpenAI (for embeddings and language model)
* Pinecone (vector database)
* Flask (web application)
* Conda (environment management)

## Project Structure

* `app.py` – Flask application entry point
* `services/` – RAG logic and vector store setup
* `data/` – Medical documents used for ingestion
* `requirements.txt` – Python dependencies
* `.env` – Environment variables (not committed to GitHub)

## Setup Instructions

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/medibot.git
   cd medibot
   ```

2. Create and activate the Conda environment:

   ```bash
   conda create -n medibot python=3.10 -y
   conda activate medibot
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the project root and add your API keys:

   ```env
   OPENAI_API_KEY=your_openai_api_key
   PINECONE_API_KEY=your_pinecone_api_key
   PINECONE_ENVIRONMENT=your_pinecone_environment
   ```

## Running the Application

Start the Flask app using:

```bash
python app.py
```

Then open your browser and access the local server URL shown in the terminal.

## Notes

* API keys should never be committed to GitHub.
* The first run may take time because embeddings are created and uploaded to Pinecone.
* This project is for educational purposes and should not be used as a substitute for professional medical advice.

## Future Improvements

* Improve response accuracy with better chunking strategies
* Add authentication and user management
* Deploy the application to a cloud platform
