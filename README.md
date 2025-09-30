# Adaptive RAG Router Chatbot

## Project Description

This project implements an **Adaptive Retrieval-Augmented Generation (RAG) router chatbot** designed for Fashion Forward Hub, an online clothing store. The chatbot intelligently routes user queries and provides contextually appropriate responses using advanced AI techniques.

## Features

### 🧠 **Intelligent Query Routing**
- **LLM-based routing**: Automatically categorizes queries as FAQ-related or product-related
- **Conditional parameter setting**: Adjusts LLM settings based on query type (creative vs. technical)
- **Multi-stage decision making**: Implements sophisticated routing logic for optimal response generation

### 🛍️ **E-commerce Integration**
- **Product database integration**: Connects to a comprehensive clothing products database via Weaviate vector database
- **FAQ handling**: Manages frequently asked questions with pre-built responses
- **Metadata extraction**: Automatically infers product attributes (size, color, category) from natural language queries
- **JSON response generation**: Produces structured product information for downstream processing

### 🔧 **Technical Architecture**
- **Vector database**: Uses Weaviate for efficient similarity search and retrieval
- **Flask API**: Provides REST endpoints for reranking and chatbot functionality
- **LLM integration**: Leverages multiple language models (Llama 3.2) via Together AI
- **Embedding generation**: Custom embedding functions for semantic search
- **Contextual augmentation**: Enriches queries with relevant product and FAQ data

### 🤖 **Chatbot Capabilities**
- **Natural conversation flow**: Maintains context and provides coherent responses
- **Product recommendations**: Suggests clothing items based on user preferences
- **FAQ resolution**: Instantly answers common customer service questions
- **Creative and technical responses**: Adapts tone and detail level based on query nature

## Project Structure

```
├── C1M4_Assignment.ipynb     # Main Jupyter notebook with implementation
├── flask_app.py              # Flask web server for API endpoints
├── utils.py                  # Utility functions for LLM interaction and processing
├── weaviate_server.py        # Weaviate database connection and setup
├── clothing_ft_format.csv    # Training data for clothing products
├── unittests.py             # Unit tests for functionality validation
├── data/                    # Data directory
│   ├── clothes.csv          # Product catalog data
│   ├── clothes_json.joblib  # Serialized product data
│   └── faq.joblib          # FAQ database
└── images/                  # Documentation images
    └── toc.png             # Table of contents reference
```

## Key Technologies

- **Python**: Core programming language
- **Weaviate**: Vector database for semantic search
- **Together AI**: LLM API service
- **Flask**: Web framework for API development
- **Jupyter Notebook**: Development and demonstration environment
- **OpenAI API**: Additional LLM integration
- **NumPy**: Numerical computing for embeddings

## Use Cases

1. **Customer Service Automation**: Handle common inquiries about shipping, returns, sizing
2. **Product Discovery**: Help customers find clothing items based on natural language descriptions
3. **Style Recommendations**: Provide outfit suggestions and fashion advice
4. **Technical Support**: Answer specific questions about product specifications and care instructions

## Getting Started

1. **Set up environment**: Install required dependencies
2. **Configure API keys**: Set up Together AI and OpenAI credentials
3. **Initialize Weaviate**: Load product and FAQ databases
4. **Run the notebook**: Execute `C1M4_Assignment.ipynb` for interactive demonstration
5. **Start Flask server**: Launch API endpoints via `flask_app.py`

This project demonstrates advanced RAG implementation techniques, combining intelligent routing, contextual retrieval, and adaptive response generation for a real-world e-commerce application.