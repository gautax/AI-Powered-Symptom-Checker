# AI-Powered Symptom Checker

## Overview
This project is an **AI-powered symptom checker** that helps users identify potential diseases based on their symptoms. It integrates **Neo4j**, **Qdrant**, and **PubMed** to provide accurate and context-aware medical insights.

## Features
- **Chatbot Interface** (Web & CLI): Users can describe their symptoms in natural language.
- **AI-Powered Analysis**: Extracts symptoms and generates Cypher queries using a fine-tuned **text2cypher-gemma** model.
- **Neo4j Integration**: Searches for diseases based on symptom relationships.
- **Vector Search (Qdrant)**: Finds relevant medical literature using semantic embeddings.
- **PubMed Data Retrieval**: Fetches and stores additional disease-related articles.
- **Google Gemini AI**: Generates conversational responses and insights.

## Technologies Used
- **Python** (Flask, Hugging Face, Neo4j, Qdrant, Google Gemini API)
- **Databases**: Neo4j (Graph Database), Qdrant (Vector Search)
- **Medical Data**: PubMed API for additional information
- **Machine Learning**: Text2Cypher model for Cypher query generation

## Installation & Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/gautax/AI-powered-symptom-checker.git
   cd AI-powered-symptom-checker
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up environment variables:
   ```plaintext
   NEO4J_URI=<your-neo4j-uri>
   NEO4J_USER=<your-neo4j-user>
   NEO4J_PASSWORD=<your-neo4j-password>
   QDRANT_API_URL=<your-qdrant-url>
   QDRANT_API_KEY=<your-qdrant-key>
   ANALYZER_API_KEY=<your-analyzer-api-key>
   ```
4. Run the Flask application:
   ```bash
   python main.py
   ```
5. Open the chatbot interface at `http://127.0.0.1:5000/`.

## How It Works
- The chatbot extracts symptoms from user input.
- It generates a Cypher query to search Neo4j for related diseases.
- If no results are found, it performs a **semantic search** in Qdrant.
- Additional medical literature is retrieved from **PubMed**.
- AI generates a user-friendly response.

## Example Usage
```
User: I've been having a fever and cough.
AI: Based on your symptoms, you might have Influenza. Common treatments include Tamiflu. Please consult a doctor.
```

## Future Improvements
- Improve AI accuracy using fine-tuned models.
- Expand disease coverage in the database.
- Add multilingual support.

## Contributors
- ENNEYA Imane
- BOUNOUAR Nouhaila
- FAKRAOUI Ayoub
- MENKARI Yahya

## License
MIT License

