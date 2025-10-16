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

    Lesson 4():
        - 


    
