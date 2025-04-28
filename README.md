# LangChain RAG with Groq, HuggingFace, and Chroma

This project demonstrates how to build a Retrieval Augmented Generation (RAG) system using LangChain, Groq, HuggingFace, and Chroma. This system allows you to ask questions about a given document and receive relevant answers.

## Project Structure

* **requirements.txt:** Lists the necessary Python packages.
* **main.ipynb:** The Google Colab notebook containing the code for the RAG system.

## How it Works

1. **Document Loading and Chunking:** The code first loads a document from a URL and splits it into smaller chunks using the `RecursiveCharacterTextSplitter`.
2. **Vector Store Creation:** It then creates a vector store using `Chroma` and embeds the document chunks using the `HuggingFaceEmbeddings` model. This enables efficient similarity search.
3. **Question Answering:** When you ask a question, the system retrieves relevant document chunks from the vector store based on semantic similarity.
4. **Answer Generation:** It uses the `ChatGroq` language model to generate an answer based on the retrieved context and your question.

## Usage

1. Install the required packages: `pip install -r requirements.txt`
2. Open the `main.ipynb` notebook in Google Colab.
3. Replace the placeholder URL with the URL of your document.
4. Run the notebook cells to load the document, create the vector store, and define the RAG pipeline.
5. Ask a question using the `graph.invoke` method, providing your question as input.
6. The system will retrieve relevant context and generate an answer.

## Dependencies

* LangChain
* Groq
* HuggingFace
* Chroma
* Sentence Transformers

## Example
