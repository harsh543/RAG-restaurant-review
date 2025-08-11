# Restaurant Recommendation RAG System 🍽️

A sophisticated Retrieval-Augmented Generation (RAG) system that provides intelligent restaurant recommendations using vector search and conversational AI.

## 🚀 Features

- **Vector-Powered Search**: Semantic similarity search using Google Gemini embeddings
- **Intelligent Recommendations**: Context-aware restaurant suggestions with explanations
- **Multi-Modal Queries**: Support for restaurant discovery, detailed reviews, and Q&A
- **Real-time Processing**: Fast vector search with Elasticsearch backend
- **Flexible Architecture**: Both direct Elasticsearch and LlamaIndex implementations


## 📊 Data Setup

The system uses a restaurant reviews dataset with the following structure:
- `business_name`: Restaurant name
- `text`: Customer review text
- `rating`: Numerical rating (1-5)
- `rating_category`: Review category (taste, menu, atmosphere, etc.)




## 🔍 System Architecture

### Core Components

1. **Vector Store**: Elasticsearch with cosine similarity
2. **Embedding Pipeline**: Text → Gemini embeddings → 768-dimensional vectors
3. **Retrieval**: KNN search for semantically similar reviews
4. **Generation**: Gemini LLM for contextual responses

### Data Flow

```
User Query → Embedding → Vector Search → Context Retrieval → LLM Generation → Response
```



## 🔧 API Functions

### `get_suggestions(query)`
Returns restaurant recommendations based on semantic search
- **Input**: Natural language query
- **Output**: JSON with restaurant names, reviews, and notes

### `restaurant_qna(name, query)`
Answers specific questions about a restaurant
- **Input**: Restaurant name and question
- **Output**: JSON with restaurant-specific answer

### `get_summary(name)`
Provides a comprehensive restaurant summary
- **Input**: Restaurant name
- **Output**: JSON with highlights, dishes, and overall rating

### `general_qna(query)`
Handles general food-related questions
- **Input**: General query
- **Output**: JSON with informative answer


## 🚀 Performance

- **Vector Dimensions**: 768 (Gemini embedding size)
- **Search Latency**: Sub-second response times
- **Index Size**: 1,100 restaurant reviews
- **Similarity Method**: Cosine similarity for semantic matching

## 🔮 Future Enhancements

- [ ] Multi-language support
- [ ] Image-based restaurant recommendations
- [ ] Real-time review ingestion
- [ ] Advanced filtering (cuisine type, price range, location)
- [ ] User preference learning
- [ ] Integration with restaurant APIs


## 🙏 Acknowledgments

- Google AI for Gemini API
- Elasticsearch for vector search capabilities
- LlamaIndex for RAG framework
- Open source community for tools and libraries
