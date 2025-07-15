# LangGraph Course Exercises

My jupyter notebook coursework for the [FreeCodeCamp](https://www.freecodecamp.org)  LangGraph Course available on YouTube [here](https://www.youtube.com/watch?v=jGg_1h0qzaM&t=3400s).

## Overview

LangGraph is a Python framework for designing and managing the flow of tasks in your application using graph structures. This course demonstrates LangGraph concepts through step-by-step exercises, agent implementations, and Jupyter notebooks.

## Highlights

<details>
  <summary>📁Sample LangGraph workflow Mermaid chart</summary>
  
  - LangGraph produces clear, insightful mermaid charts that make it easy to visualize and troubleshoot the Agent flow.
  - From [From the Dual Condition Notebook:](https://github.com/smagara/LangGraph-Coursework/blob/main/langgraph_dual_condition.ipynb)
  
  ![image](https://github.com/user-attachments/assets/5e2a8b7f-5310-4938-9659-04b01154e564)
</details>

<details>
  <summary>📁Agentic RAG, example where the LLM uses a PDF as a knowledge source</summary>
  
  - Python code splits the document into chunks...
  - ..then creates a vector store for lookups from the LLM:

  - [📔 Display RAG Jupyter Notebook](https://github.com/smagara/LangGraph-Coursework/blob/main/langgraph_RAG_agent.ipynb)
</details>

<details>
  <summary>📁Simple ChatBot, with remembered conversational history</summary>

  - Note that in this example, the 2nd query about "wobble" would be ambiguous without the prior history of the RNA question

  - [📔 Display ChatBot Jupyter Notebook](https://github.com/smagara/LangGraph-Coursework/blob/main/langgraph_simplechatbot.ipynb)
</details>

<details>
  <summary>📁ReAct Agent, iteratively reasoning and acting by observing the results of Tools in the LangGraph flow and adjusting accordingly</summary>

  - The Tools are primative examples, each Python ```@tool``` function performs an arithmetic operation

  - The notebook exercises our tools:
    ``` python
    def add(a: int, b: int)
    def subtract(a: int, b: int)
    def mult(a: int, b: int)
    ``` 
    And demonstrates that the LLM will use the tools if they make sense, but will fall back on its training when the tools are of no use, for example to tell a joke: 
    ```
    Add 34 + 21.  Then multiply 12 by 22.  Also subtract 23 from 88 then tell a joke
    ```
    Reply from the AI:
    ```
    Here are the results of your calculations:

    1. 34 + 21 = 55
    2. 12 * 22 = 264
    3. 88 - 23 = 65

    Now, here's a joke for you:

    Why don’t scientists trust atoms? 

    Because they make up everything!
    ```


  - [📔 Display ReAct Agent Jupyter Notebook](https://github.com/smagara/LangGraph-Coursework/blob/main/langgraph_react_agent_tools.ipynb)
</details>