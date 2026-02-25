# n8n LinkedIn Automation 🚀

This project is an advanced n8n-based automation designed to generate high-quality LinkedIn posts and cover images using Retrieval-Augmented Generation (RAG). The system ensures brand consistency by retrieving specific guidelines and historical data before generating content.

# 🧠 System Architecture

The workflow follows a sophisticated logic to ensure every post aligns with professional standards:

Trigger: Initiated via n8n (Manual/Webhook).

Context Retrieval (RAG): The AI agent queries a Pinecone vector database.

Prompt Augmentation: The agent injects retrieved rules into the LLM prompt.

Fallback Mechanism: If the RAG store returns no relevant results, the system automatically falls back to pre-defined professional defaults to ensure the workflow never fails.

# 🛠️ RAG Setup Instructions (Pinecone)

To replicate the environment or verify the task, use the following configuration:

Index Name: linkedinautomation

Namespace: default

Embedding Model: text-embedding-3-small

Vector Dimension (TopK): 1536

# Data Population

Ensure you upload the provided .txt documents (located in this repo) into the Pinecone index. The system is specifically optimized to retrieve:

Tone Guidelines: Maintains a consistent brand voice.

Formatting Rules: Ensures correct spacing and readability.

Hashtag Rules: Applies strategic tagging logic.

Sample Posts: Uses few-shot learning to mimic successful past content.

# ⚙️ How to Use

Import the .json file into your n8n instance.

Configure Credentials for OpenAI and Pinecone.

Populate Pinecone with the provided text files using the settings mentioned above.

Execute the workflow to generate structured LinkedIn content.
