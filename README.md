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

### Lesson 5 - Router 
In this lesson, I learned how the model can smartly decide when to use a tool and when to answer on its own. I tried adding a simple tool and saw how the LLM used it only for relevant questions while replying directly for others. This helped me understand how routing works and how the model balances its own reasoning with tool usage and i have attached the screenshot of the langgraph studio in the refrence notebook

*Refrence notebook* - https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%201/router.ipynb

*My work* - Here i had done a lttle bit of twerking by modifieng my function to a power function which gives power and also did some changes in router.py in studio folder so that it gives me a proper understanding of my routes in langgraph studio and i have attached screenshot for the same 
https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%201/router_mywork.ipynb

### Lesson 6 - Agent 
In this lesson, I learned how to build a simple agent using multiple arithmetic tools following the ReAct architecture. I saw how the model thinks, calls the right tools, observes the results, and continues the process step by step to solve a multi-step arithmetic problem. This helped me understand how LangGraph allows the model to reason dynamically in a loop and decide when and how to use tools intelligently.

*Refrence notebook* - https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%201/agent.ipynb

*My work* - Here i had done a lttle bit of twerking by modifieng my airthmatic calculator and added more function such as modulus and substraction and did the whole process again and trace the graph at lagsmith tracing .The model handled multi-step reasoning well, chaining tools as needed. and i have added screenshots for the same.
https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%201/agent_mywork.ipynb

### Lesson 7 - Agent_Memory
In this lesson, I learned how to add memory to agents using a thread ID that helps them remember previous interactions. This allowed the agent to answer follow-up questions with proper context and maintain continuity across multiple queries. I also discovered that LangGraph’s dev mode has a built-in persistence layer, which automatically manages memory and tracks past states without any manual setup.

*Refrence notebook* - https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%201/agent-memory.ipynb

*My work* - Here I did a little bit of tweaking by extending my Airthmatic operation set and testing memory with a thread where the final question depended on earlier steps. The model successfully referenced previous results, showing memory retention works, and I also confirmed that LangGraph Studio’s built-in persistence layer handles memory automatically. I have added screenshots for the same.
https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%201/agent_memory_mywork.ipynb

### Lesson 8 - Deployment (optional)
Here I didn’t implement anything since LangSmith Deployment is only available for Plus users and this lesson was optional. I just went through the video to understand the concept. I learned how to move beyond local development and deploy a LangGraph application as a service or API, including packaging the graph, managing secrets and environment variables, enabling persistence, and exposing graph endpoints for external use.

# Module 2 State and memory
The module’s main focus is on how to represent, maintain and manipulate the “state” of an agent or workflow built with LangGraph. The “state” refers to the structured data that captures what the agent knows / what has happened so far.

### Lesson 1- State schema
In this video, I learned that a schema defines the structure and data types used in a graph. We have been using TypedDict for this purpose and also explored dataclasses, which are similar but access values using the dot operator. Both TypedDict and dataclasses do not enforce type hints at runtime, allowing invalid data. To solve this, Pydantic is used as it provides automatic data validation.

Refrence notebook(modified) - https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%202/state-schema.ipynb

*My work* - I created a custom graph that determines whether the user intends to confirm or cancel an order using Pydantic for data validation. I then observed its behavior with both valid and invalid inputs.
 
 https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%202/State_schema_mywork.ipynb

 # Module 3 UX and human-in-the-loop

 ### Lesson 1 - Streaming
In this video, I got a grasp of the concept of streaming. There are two kinds of streaming: streaming values and streaming updates. Streaming values allow for the complete state of the graph to be viewed after every node is invoked, while streaming updates merely show the changes to the state of the graph after each node is called. Furthermore, I discovered that it is possible to stream tokens as they are produced by the method .astream_events, which is responsible for emitting events that happen inside at the nodes. Each event is a dictionary that contains the event, the name, the data, and the metadata (which has langgraph_node). Also, I found out how to stream tokens with the help of the LangGraph API. In addition, the IDE was used to explore the LangGraph API application, which included the new streaming method messages that updates the final message token by token and provides the output. I have added screenshot for langgrapgh platform also.

Refrence notebook(modified) - https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%203/streaming-interruption.ipynb

*My work*- In this notebook there was nothing much to do so i modified the examples and questions asked to chatbot such as Tell me about first world war and run all the steps above. I also done this in langgraph platform , you can see this in notebook given below 
https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%203/streaming-interruption_mywork.ipynb

### Lesson 2 - Breakpoint
In this notebook, we explored how LangGraph supports human-in-the-loop AI workflows through breakpoints. We learned to build a simple agent that can perform arithmetic operations, pause execution before using a tool, inspect its internal state, and then either resume or stop. This helped us understand how breakpoints facilitate approval, debugging, and state editing — essential for creating transparent and controllable AI systems. We also observed how LangGraph handles memory checkpoints, enabling an agent to pause and resume smoothly.

Refrence notebook(modified) -  https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%203/breakpoints.ipynb

*My work*- I simply modified this agent to do more calculations and added more mathematical operations  and added more acurate statements to provide reasoning at each step
https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%203/breakpoints_mywork.ipynb

### Lesson 3  - Editing state and human feedback
In this video, I learned how to edit the graph state after an interruption in the flow. Breakpoints allow modifying the graph’s state through the default “add_message” reducer. I explored adding interrupts in LangGraph Studio and editing the graph state via the LangGraph API. Lastly, I learned to use a dummy node with the “as_node” field to inject user input dynamically into the graph.

Refrence notebook(modified) -  https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%203/edit-state-human-feedback.ipynb

*My work* - In this example, I added more mathematical tools like subtract and divide. I also included tools for motivation and focus.I interrupted and changed the state of the graph using both hardcoded values and user input. Additionally, I modified the graph’s state using the LangGraph API. and i have visualized it in lagsmith studio. 
https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%203/edit_state_human_feedback_mywork.ipynb
(attached screentshot too)

### Lessson 4 - Dynamic Breakpoints
In this video, I learned that we can create dynamic breakpoints that allow the graph to interrupt itself automatically based on a condition in its state. This acts like an internal pause trigger without needing manual intervention. We use NodeInterrupt to achieve this. However, to continue execution, we must update the state, or else the graph will keep pausing at the same point repeatedly.

Refrence notebook(modified) -  https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%203/dynamic-breakpoints.ipynb (by mistakenly i have written video 3 in commit)

*My work* - I modified it so that the graph now pauses dynamically after a certain number of steps, by using a step_count value inside the graph state. When step_count reached the set threshold, the graph interrupted itself. To resume execution, I reset the step_count and updated the state before calling graph.stream() again.
https://github.com/ShreeGattani/ShreeGattani-langgraph-MAT496/blob/main/Module%203/dynamic_breakpoints_mywork.ipynb



