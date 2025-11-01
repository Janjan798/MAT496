Langsmith Foundations Course:
Module 0:
    - Setup API keys and checked working of langsmith

Module 1:
    Lesson 1(tracing_basics.ipynb):
        - Learnt hierarchy of project->traces->runs
        - Learnt what tracing is for and how to trace statically and during runtime
        - Learnt how to filter and check metadata in langchain website

        - CHANGES MADE:
            - Added another code block where it asks how many seasons are there in a tv show gets the answer
            and then logs it as metadata for that trace.

    Lesson 2(types_of_runs.ipynb):
        - Learnt about the different types of runs
        - Learnt why these runs make a difference by going on the website and seeing what hapens if we
        specify the run_type

        -CHANGES MADE:
            -Changed run type for a llm trace to tool to see what happens
            -Nothing website still rendered output as if it were done by a llm
    
    Lesson 3(alternative_tracing_methods.ipynb):
        - Learn about the alternatives to @traceable
        - If we are using OpenAI SDK its easier and logical to use their OpenAI_Wrap
        - Can also use with trace() which is built into python and gives us more granular control

    Lesson 4(converstational_threads.ipynb):
        - Learnt about threads and using UUID for threads
        - Learnt about why threads are useful by checking my project on langchain website and filtering
        by thread

        -CHANGES MADE:
            - Experimented by changing the messages to the llm about me

----------

Module 2:
    Lesson 1(dataset_upload.ipynb):
        - Learnt about the concept of dataset in Langsmith
        - Learnt multiple ways of adding examples to the dataset
        
        -CHANGES MADE:
            - Added my own example at the bottom

    Lesson 2(evaluators.ipynb):
        - Learnt how evaluators calculate metrics based on a run and an example.
        - We can define evaluators directly in out code or else in langsmith UI

        -CHANGES MADE:
            - Added my own example to test how the similarity score works when answer is half right.

    Lesson 3(experiments.ipynb):
        - Experiments- running application over a dataset and evaluating its performance
        - Can be run locally in code 
        - Can be run over whole datasets, specific versions or splits.
        - Can be run with other parameters repetitions,concurrent threads, metadata.

        -CHANGES MADE:
            - Tweaked it to run a split i had created called base split instead of runnning on inital dataset

    Lesson 4:
        - Learn how to compare experiments on the Langsmith UI
        - Learnt how to filter and check the evaluators functioning in the UI as well

        -CHANGES MADE:
            - No code so just meddled with the filters in the UI

----------

Module 3:
    Lesson 1(playground_experiments.ipynb):
        - Walked through functionality of Langsmith Playground
        - Uploaded dataset from code to langsmith and used it to check on playground
    
        -CHANGES MADE:
            - Changed the questions uploaded(dataset)

    Lesson 2:
        - Walked through prompt hub and how it works
        - How to create and commit changes to a prompt on the UI
        - How to push commits using the SDK

    Lesson 3(prompt_engineering_lifecycle.ipynb)
        - Went through an end to end example on prompt hub
        - Learnt how to iterate a prompt

    Lesson 4:
        - Prompt canvas lets us ask the agent to write update or comment on existing prompts

        -CHANGES MADE(for lesson3 and 4):
            - Worked in the UI
            - Changed the quick actions filters in prompt canvas

----------

Intro to Langgraph:
Module 1:
    Lesson 1:
        - An agent is basically a control flow set by a LLM
        - Langgraph helps you increase the reliability of agents when you give them more control
        - Intro lesson so no changes/code

    Lesson 2(simple-graph.ipynb):
        - Learnt about the core components of langgraph and how to make a simple graph

        -CHANGES MADE:
            - Added a node4 and changed the probabilities to 33% for each node

    Lesson 3:
        - Basic Introduction to how we will be using Langsmith studio
        - No Code changed the graph state in the UI and watched the thread

    Lesson 4(chain.ipynb):
        - Learnt how to use chat messages and models in out graph
        - Learnt to bind tools to our chat model and execute tool calls in graph nodes

        -CHANGES MADE:
            - Added another tool call which raise a to the power of b and checked the output

    Lesson 5(router.ipynb):
        - Learnt how to make a simple router which decides between a tool call and a NLM
        - Learnt how to check the graph on Langsmith studio

        -CHANGES MADE:
            - Changed the message from multiplication to a question about me to check if it still called the tool
            - It also doesnt work perfectly as if you also ask what is 2 raised to the power of 3, it gets confused and messes it up


    Lesson 6(agent.ipynb):
        - Learnt how to set up an agent
        - Basically routing the tools back to the LLM in a loop so that the llm can think and act upon the output

        -CHANGES MADE:
            - Added a power tool function and changed the human message to see if it works

    Lesson 7:
        - Learn how to make the agent remember the output of a previous humanmessage
        - Done by using threads - a collection of checkpoints (referenced by thread id)

----------

Module 2:
    Lesson 1(state-schema.ipynb):
        - Learnt how to specify the schema of graph. the structure and types of data a graph will use
        - Typedict and Dataclasses doesnt enforce datatype validation during runtime
        - Learnt how to use pydantic to set up state schema for graphs and do data validation

        -CHANGES MADE:
            - Added my own pydantic state schema which checks the 'sex' argument, and validates between 'a man' % 'a woman'

    Lesson 2(state-reducers.ipynb):
        - In graphs trying to update the same value more than once in the same step wont work as its ambiguous for the graph to decide which state to keep
        - Hence we use Reducers, to specify how to perform the updates
        - Can also use custom reducer states to handle specific values like null values

        -CHANGES MADE:
            - Changed the inputs and update values for the first simple graph with the add operator
    
    Lesson 3(multipe-schemas.ipynb):
        - Learnt about overall state and private states
        - The nodes of a graph have information which may not be relevant to the input/output and hence we use private states to have more contol over what the user sees in input time
        - Learnt how to define explicit input and output schemas for a graph

        -CHANGES MADE:
            - Added another node so made the graph 3 nodes instead of 2, to increment using private state once more

    Lesson 4(trim-filter-messages.ipynb):
        - Long running chat converstation have high token usage
        - To optimize we can remove/filter/trim the messages going to the llm

        -CHANGES MADE:
            - Added another human message asking about blue whales after narwhals while filtering the latest message to the llm

    Lesson 5(chatbot-summarization.ipynb):
        - Learn how to produce a running summary of the conversation
        - Used threads like we learnt in module 1 to give the llm memory using a collection of checkpoints

        -CHANGES MADE:
            - Changed the input to the llm giving details about me and checked the summary

    Lesson 6(chatbot-external-memory.ipynb):
        - Learnt how to persist the messages locally using SQLITE
        - Used Langsmith Studio also to go through the same

        -CHANGES MADE:
            - Changed the input to the llm giving details about me and checked if the messages persisted locally
            - Went into langsmith studio and saw how and when it triggered the summarize conversation node 

----------

Module 3:
    Lesson 1(streaming-interruption.ipynb):
        - Streaming outputs/messages from the chat model whether they are tool calls or just natural language responses
        - 2 different streaming modes(values, updates)
        
        -CHANGES MADE:
            - Changed the input prompts and the thread ids of the prompts

    Lesson 2(breakpoints.ipynb):
        - Breakpoints allow us to stop the graphs at specific states
        - You can make it interrupt before a node or after
        
        -CHANGES MADE:
            - Added powerof tool and used that to check the interrupt before

    Lesson 3(edit-state-human-feedback.ipynb):
        - Learnt how to change the human message after stopping at a breakpoint

        -CHANGES MADE:
            - Added new tool which calculates the remainder
            - Made the input prompt to the llm have more steps to and saw how it stopped after each point
    
    Lesson 4(dynamic-breakpoints.ipynb):
        - Dynamic breakpoints, how to make the graph interrupt itself, like on a condition
        - We do this using NodeInterrupt
        
        -CHANGES MADE:
            - Changed the dynamic breakpoint to get triggered if a number greater than 5 is inputted

    Lesson 5(time-travel.ipynb):
        - We can re run our agent from any of the prior steps by passing a checkpoint id and thread id
        - Learnt the difference between replaying and reexecuting

        -CHANGES MADE:
            - Added subtract tool
            - Changed the input to the forked prompt

----------
    
Module 4:
    Lesson 1(parallelization.ipynb):
        - Learnt how parallelization works between nodes and how to set your own order for state updates
        - Learnt how to gather context from two different souces for a question and make the llm answer with context
    
        -CHANGES MADE:
            - Added new states in the graph with the custom reducers

    Lesson 2(sub-graph.ipynb):
        - Learnt how to integrate subgraphs with your use case
        - Graphs communicate with each other using overlapping keys, the keys are what each graph can access from one another
        - It was a toy subgraph so did not make changes

    Lesson 3():
        - 
