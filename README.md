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

    Lesson 4(converstational_threads.ipynb):
        - Learnt about threads and using UUID for threads
        - Learnt about why threads are useful by checking my project on langchain website and filtering
        by thread

        -CHANGES MADE:
            - Experimented by changing the messages to the llm about me


Module 2:
    Lesson 1(dataset_upload.ipynb):
        - Learnt about the concept of dataset in Langsmith
        - Learnt multiple ways of adding examples to the dataset
        
        -CHANGES MADE:
            - Added my own example at the bottom

    Lesson 2():
        - Learnt how evaluators calculate metrics based on a run and an example.
        - we can define evaluators directly in out code or else in langsmith UI

        -CHANGES MADE:
            - Added my own example to test how the similarity score works when answer is half right.

    Lesson 3():
