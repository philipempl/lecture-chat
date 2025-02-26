# Lecture Chat

## Introduction

The Lecture Chat project is designed to offer valuable information and assistance on lectures. It utilizes various resources like lecture slides, screencasts, PDFs, and YouTube links to provide comprehensive answers to user questions. Notably, each response includes citations and links to the relevant source material, ensuring a deeper understanding and access to additional insights.

## Requirements

1. **On-Premise Solution**: The chatbot operates on an on-premise infrastructure to minimize costs and ensure data privacy.

2. **Docker Containers**: Docker containers are employed for easy deployment and management of services.

3. **Open Source Development**: The development of the chatbot exclusively utilizes open-source solutions.

## Development Resources

- Programming Language: Python
- [Docker Compose](https://www.docker.com/blog/build-and-deploy-a-langchain-powered-chat-app-with-docker-and-streamlit/)

### LLM Chaining

- [LangChain](https://github.com/langchain-ai/langchain)

### Langchain Low-Code No-Code

- [Langflow for Langchain Python](https://github.com/logspace-ai/langflow)

### Local Deployment of LLMs on CPU

- [Ollama](https://github.com/jmorganca/ollama)
- [Llama2](https://ai.meta.com/llama/)

### Python UI

- [Streamlit](https://github.com/streamlit/streamlit)

### (Vector) Databases

- [ChromaDB](https://github.com/chroma-core/chroma)

### Other Links

- [Citations](https://medium.com/@yotamabraham/in-text-citing-with-langchain-question-answering-e19a24d81e39)
- Search Platform: [Jina](https://github.com/jina-ai/jina)
- Service for Langchain: [Langchain Serve](https://github.com/jina-ai/langchain-serve)

## Deployment

Follow these steps to run the provided services using Docker Compose:

1. **Install Docker and Docker Compose:**

   Ensure that Docker and Docker Compose are installed on your system. If not, you can download and install them from the official Docker website: [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/install/).

2. **Clone the Repository:**

   Clone this repository to your local machine.

3. **Start Services:**

   Start the services defined in the `docker-compose.yml` file using the following command:

   ```bash
   docker-compose up -d
   ```

   The `-d` option stands for "detach" mode, which runs the services in the background.

4. **Access User Interfaces:**

   After starting the services, you can access the various user interfaces using the following URLs:

### Accessible User Interfaces (UIs)

1. **Lecture Chat Interface (`lecture-chat`):**

   The Lecture Chat interface is accessible via a web browser by visiting:

   ```
   http://localhost:8080
   ```

   This interface allows interaction with the Lecture Chat Bot.

2. **Language Processing Tool Interface (`langflow`):**

   The Language Processing Tool interface can be accessed at:

   ```
   http://localhost:7860
   ```

   Here, the functions of the `langflow` service for language processing are available.

3. **Code Syntax Highlighting Interface (`chroma`):**

   The interface for the code syntax highlighting service is reachable at:

   ```
   http://localhost:8000
   ```

   This interface allows testing and using the `chroma` service's code syntax highlighting functions.

### Stopping the Services

To stop and remove the services, execute the following command in the directory containing the `docker-compose.yml` file:

```bash
docker-compose down
```

This will stop the services and remove the associated containers, networks, and volumes.

## License

This project is released under the [MIT License](https://github.com/philipempl/lecture-chat/LICENSE).
