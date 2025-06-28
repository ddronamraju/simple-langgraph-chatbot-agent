# LangGraph based Agent Chatbot
- Chatbot that takes user prompt for the type of agent and the corresponding question
- Streamlit UI
- FastAPI to generate end points for seamless interaction between UI and the server
- Pydantic data model to validate input and output formats
- Type hinting for code readability and static analysis
- LangGraph as the Agentic AI framework
- Docker for deployment

- Docker Instructions
    - Build image
        - docker build -t simple-langgraph-agent .
    - Build a container using image
        - docker run -d --env-file .env -p 8000:8000 -p 8501:8501 --name simple-langgraph-agent-container simple-langgraph-agent
    - Push image to docker hub
        - login to hub.docker.com, find your username- ddron
        - Open terminal
            - docker tag simple-langgraph-agent ddron/simple-langgraph-agent:latest
        - Push image
            - docker push ddron/simple-langgraph-agent:latest
    - Pull image
        - docker pull ddron/simple-langgraph-agent:latest
    - Run pulled image anywhere
        - docker run -d -p 8000:8000 -p 8501:8501 --name new_simple-langgraph-agent-container new_simple-langgraph-agent


