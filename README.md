# ShreeGattani-langgraph-MAT496
All I learned in langgraph course from langchain academy 

# Module 1 
In this module we will introduce several generic agent architecture and some common challenges faced by developers in building agents . 
We will discuss why building custom agents with domain specific workflows and focus on high reliability is really important.
Finally we will show how langgraph makes it easy to build these custom agents 

### Lesson 1 - Motivation 
In this lesson, I learned why LangGraph is valuable for building more complex LLM applications. Instead of working with simple, linear chains, LangGraph enables the creation of dynamic, graph-based workflows with loops, branching, and shared state. This makes it much easier to design agent-like systems that can make decisions, use tools, and adapt during execution. It also improves debugging and scalability by offering better visibility into the workflow.

*My work* - There was no code provided in this video—it primarily focused on basic and introductory concepts.

### Lesson 2 - Simple Graph
In this lesson , I learned how to define state of the graph , what is node and defining nodes and defining edges as well as conditional edges then constructing graph with the help of these components using special nodes such as start and end then compiling graph to see mermaid diagram .Then using invoke method (`invoke` runs the entire graph synchronously) to invoke the graph and then visualising it in langgraph platform in the langsmith studio. I had run the provided jupyter notebook and here is the link for that -

 Refrence notebook(modified) - https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%201/simple-graph.ipynb

 *My work* - Here i did a little bit of *twerking* with changing some questions to intelligent and dunb editing my name , and repeated all the steps like provided in the refrence 
 notebook. 
 https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%201/simple_graph_mywork.ipynb

### Lesson 3 - Langsmith Studio
In this lesson , I learned how to visualize graph in langgraph studio which is an interactive IDE for building, visualizing, and debugging AI agent workflows and get familier with all the features provided by langgraph studio and then i had attached screenshots of what i observed in a refrence notebook .

*Refrence notebook* - https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%201/langsmith_studio.ipynb

### Lesson 4 - Chain
In this lesson , i have leared a brief about building a simple chain that combines chat messages as our graph state , using chatmodels in graph nodes , binding tools to chatmodel and executing tool calls in graph nodes . I saw how Chat models can use messages which capture different roles within a conversation , using tools which is useful whenever you want model to interact with external system , about reducres and finally visualizing the graph.

*Refrence notebook* - https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%201/chain.ipynb

*My work* - Here i provided different questions and answers about space and i have added a tool calculator that can do 4 operations  addition , substraction , multiply , division  and tried asking the question for same . i have also used reducers so that messages can not be overriden and then finally i obsereved out graph and then some questions to the model in graph .
https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%201/chain_mywork.ipynb

