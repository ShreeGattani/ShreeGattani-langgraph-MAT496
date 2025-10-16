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

