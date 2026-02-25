RAG Setup Instructions

1. Pinecone Index Name: linkedinautomation
2. Namespace: default
3. Embedding Model: text-embedding-3-small
4. TopK: 1536

Upload the provided .txt documents into the Pinecone index.

The AI agent is configured to:
- Retrieve tone guidelines
- Retrieve formatting rules
- Retrieve hashtag rules
- Retrieve sample posts

If retrieval returns no relevant results, the system falls back to professional defaults.