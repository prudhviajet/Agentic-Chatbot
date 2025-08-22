### End to End Project Agentic AI Chatbots

flowchart TD
    U[User Input via Streamlit UI] --> F[UI Layer]

    F --> |User Message| E[(groqllm)]

    E --> B[GraphBuilder]
    B --> C[(state)]
    B --> D[Basic Chatbot]
    D --> M[START]
    M --> N[(node.basic_chatbot_node)]
    N  --> P[END]

    P --> R[Generate Response]
    R --> O[Display Result in UI]

    subgraph graph
        B
        C
        D
    end

    subgraph basic_chatbot_build_graph 
        M 
        N 
        P  
    end

    subgraph LLMS
        E
    end

    subgraph UI
        F[uiconfigfile & streamlitui.loadui]
        O[streamlitui.display_result]
    end