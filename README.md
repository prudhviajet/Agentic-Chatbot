### End to End Project Agentic AI Chatbots

flowchart TD
    A[main.py (Entry Point)] --> B[Graph Builder]
    B --> C[State Management]
    B --> D[Nodes (Chatbot Logic)]
    D --> E[LLM Integration]
    A --> F[UI Layer]
    F --> G[Streamlit UI]
    G --> H[Display Result]
    G --> I[Load UI]
    F --> J[UI Config File]
    
    subgraph Graph
        B[graph_builder.py]
    end

    subgraph State
        C[state.py]
    end

    subgraph Nodes
        D[basic_chatbot_node.py]
    end

    subgraph LLMS
        E[groqllm.py]
    end

    subgraph UI
        F[uiconfigfile.py]
        J[uiconfigfile.ini]
        G[streamlitui]
        H[display_result.py]
        I[loadui.py]
    end