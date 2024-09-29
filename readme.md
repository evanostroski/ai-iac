# Hi! 👋
This project aims to simplify creating a *local* LLM development 
environment while including tools for RAG and observability.

## Includes
- [Ollama](https://github.com/ollama/ollama) - run local large language models
- [Open WebUI](https://github.com/open-webui/open-webui) - Open WebUI for Ollama
- [Langflow](https://github.com/langflow-ai/langflow) - Low-code app builder for RAG and multi-agent AI applications
- [Langfuse](https://github.com/langfuse/langfuse) - Traces, evals, prompt management and metrics to debug and improve your LLM application
- [Milvus](https://github.com/milvus-io/milvus) - a high-performance, highly scalable vector database
- [Attu](https://github.com/zilliztech/attu) - The GUI for Milvus

## Requirements
- [Docker](https://docs.docker.com/get-started/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Instructions
1. Rename `.env-example` to `.env` and set your environment variables
2. Run `docker compose up` in the same directory as the `docker-compose.yml` file from this project
3. Ollama is configured to use any NVIDIA GPUs. Make sure that your GPU is available to Docker containers by installing [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#installation)

## Usage
1. Use WebUI to download models for Ollama
2. Use service names for internal URIs
    - http://milvus:19530
    - http://ollama:11434
    - http://langfuse:3000
3. Langflow uses default Milvus database and creates collections automatically.  
4. Use Attu to drop collections from Milvus if you change the embedding model / vector index dimensions
5. You won't have `LANGFUSE_SECRET_KEY` and `LANGFUSE_PUBLIC_KEY` on the first go.  If you want to use Langfuse, compose up, provision an API key from Langfuse, compose stop, add your key to `.env` and compose start again. 😅

## UI links
- Attu ( [http://localhost:8000](http://localhost:8000) )
- Langflow ( [http://localhost:7860](http://localhost:7860) )
- Langfuse ( [http://localhost:3000](http://localhost:3000) )
- Open WebUI ( [http://localhost:3001](http://localhost:3001) )