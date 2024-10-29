# Travel Chatbot using Retrieval-Augmented Generation (RAG)

Welcome to the Travel Chatbot project! This chatbot uses Retrieval-Augmented Generation (RAG) to provide contextually aware responses to travel-related questions. Built with OpenAI’s GPT language model and Pinecone’s vector database, it offers accurate answers about flight details, layovers, and passenger information based on user journey data.

## Project Overview
The chatbot leverages:
- **Pinecone Vector Database**: Stores and retrieves travel data as vector embeddings for fast and relevant responses.
- **OpenAI Language Model**: Generates coherent responses based on retrieved journey details, enhancing user interaction with contextually relevant information.

## Features
- **Flight Details**: Retrieve accurate flight timings, airport details, and seat information.
- **Layover Information**: Calculate and display layover times for user journeys.
- **Baggage Information**: Check baggage allowances and other passenger-specific data.
  
## Project Structure
- **`data/`**: Contains the JSON file with journey details.
- **`src/`**: Holds the main code, including data ingestion and chatbot functions.
- **`hava havai intern.ipynb`**: Development notebook for testing and refining functions.

## Getting Started

### Prerequisites
Ensure you have the following:
- Python 3.7 or higher
- API keys for **Pinecone** and **OpenAI**

### Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/travel-chatbot-rag.git
   cd travel-chatbot-rag


Usage
Data Ingestion
Load Data into Pinecone: Run data_ingestion.py (or the corresponding cells in hava havai intern.ipynb) to ingest the JSON travel data into Pinecone.
Index Creation: Ensure each segment of flight data is indexed in Pinecone for efficient retrieval.
Running the Chatbot
To use the chatbot for answering travel-related queries, run the main script or use the Jupyter notebook:

python
Copy code
from chatbot import handle_question

query = "What time is my flight from Cape Town to Addis Ababa?"
response = handle_question(query)
print(response)
Example Queries
Flight Time: “What time is my flight from Cape Town?”
Layover: “What’s my layover duration?”
Baggage Allowance: “Do I have checked baggage for my flight?”
Code Overview
data_ingestion.py: Loads travel journey data into Pinecone with vector embeddings and metadata for query-based retrieval.
chatbot.py: Main chatbot functionality to handle specific travel queries and retrieve accurate responses using RAG.
helper_functions.py: Contains utility functions for vector generation, query processing, and metadata handling.
Future Enhancements
Expanded Query Types: Support for more complex travel-related questions.
User Authentication: Personalize responses based on authenticated user data
