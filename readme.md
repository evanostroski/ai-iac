# Hi!
---
This project aims to simplify creating a *local* LLM development 
environment while including tools for RAG and observability.

## Includes
- [Ollama](https://github.com/ollama/ollama) - run local large language models
- [Open WebUI](https://github.com/open-webui/open-webui) - offline WebUI
- [Langflow](https://github.com/langflow-ai/langflow) - Low-code app builder for RAG and multi-agent AI applications.
- [Milvus]() - a high-performance, highly scalable vector database
- [Attu](https://github.com/zilliztech/attu) - The GUI for Milvus

## Requirements
- [Docker Compose](https://docs.docker.com/compose/install/)

## Instructions
1. Set `DOCKER_VOLUME_DIRECTORY` in your environment
2. Run `docker compose up` in the same directory as the `docker-compose.yml` file from this project

## Usage
1. Use WebUI to download models for Ollama
2. Use service names for internal URIs
    - http://milvus:19530
    - http://ollama:11434
3. Langflow uses default Milvus database and creates collections automatically.  
4. Use Attu to drop collections from Milvus if you change the embedding model / vector index dimensions

## UI links
- Attu ( [http://localhost:8000](http://localhost:8000) )
- Langflow ( [http://localhost:7860](http://localhost:7860) )
- Open WebUI ( [http://localhost:3000](http://localhost:3000) )