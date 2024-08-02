# Intelligent Movie Recommendation Assistant

## Overview

The Intelligent Movie Recommendation Assistant is a chatbot designed to provide movie recommendations and information using advanced language models and graph databases. This project integrates a Large Language Model (LLM) with a Neo4j graph database to deliver intelligent responses based on movie data. The application is built using Streamlit for the web interface and LangChain for the integration of LLMs and Neo4j.

## Features

- **Movie Recommendations:** Provide personalized movie recommendations based on user queries and movie plots.
- **General Chat:** Engage users in conversations about movies, actors, directors, and related topics.
- **Plot-Based Search:** Retrieve and recommend movies based on specific plot descriptions.
- **Conversational Memory:** Maintain context and history of user interactions to offer more relevant responses.

## Technologies Used

- **Streamlit:** An open-source Python library for creating web applications with minimal effort. Used for building the frontend of the chatbot.
- **LangChain:** A framework for integrating LLMs with various data sources and tools. Used for managing the interaction between the chatbot and the LLM.
- **Neo4j:** A graph database used for storing and querying movie data. Provides advanced capabilities for recommendation and similarity searches.
- **OpenAI GPT-4:** A large language model used for generating responses and recommendations.
- **Python:** The programming language used for implementing the application logic and integration.

## Setup and Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-repo/intelligent-movie-recommendation-assistant.git
   cd intelligent-movie-recommendation-assistant
   
2. **Create a Virtual Environment:**
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

3. **Install Dependencies:** 
  ```bash
  pip install -r requirements.txt

4. **Setup Secrets:**
Create a file .streamlit/secrets.toml and add your OpenAI and Neo4j credentials:
  ```bash
  OPENAI_API_KEY = "your-openai-api-key"
  OPENAI_MODEL = "gpt-4"
  NEO4J_URI = "your-neo4j-uri"
  NEO4J_USERNAME = "your-neo4j-username"
  NEO4J_PASSWORD = "your-neo4j-password"

5. **Run the Application:**
  ```bash
  streamlit run bot.py

## Project Structure

bot.py: Main entry point for the Streamlit application.
llm.py: Initializes the LLM and embeddings.
graph.py: Manages the connection to the Neo4j database.
agent.py: Contains the logic for the chatbot agent, including tools and handlers.
tools/vector.py: Defines the retrieval tools for movie plot search.
tools/cypher.py: Contains Cypher queries used for interacting with the Neo4j database, including queries for movie recommendations and plot searches.
.streamlit/secrets.toml: Stores sensitive configuration information.

## Usage

General Chat: Ask the chatbot any movie-related question. It will provide information based on its training and the data in the Neo4j database.
Plot-Based Search: Describe a movie plot to get recommendations of similar movies.
Conversation History: The chatbot maintains conversation history to provide contextually relevant responses.
