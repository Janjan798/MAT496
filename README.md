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
            -changed run type for a llm trace to tool to see what happens
            -nothing website still rendered output as if it were done by a llm
    
    Lesson 3(alternative_tracing_methods.ipynb):
        - Learn about the alternatives to @traceable
        - If we are using OpenAI SDK its easier and logical to use their OpenAI_Wrap
        - Can also use with trace() which is built into python and gives us more granular control
