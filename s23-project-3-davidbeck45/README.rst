Short Description:
  The project focuses on implementing a parallel zip (pzip) program using the C programming language and POSIX-threads (pthreads) library. The pzip program reads an input text file consisting of lowercase letters (a-z) only and produces a binary file indicating the consecutive occurrences of each character. The parallelization is achieved through the use of pthreads.

Project Structure
1. Project Description
  1.1 Objectives
    Use multiple threads to complete a computational task faster.
    Familiarity with running concurrent threads using the pthreads library.
    Sharpen systems programming skills through practical project work.
  1.2 Summary
    The project involves implementing a parallel zip program using C and pthreads. The program reads an input file, processes it in parallel, and produces a binary file indicating consecutive character occurrences.

  1.3 Functionality
    The main functionality involves implementing the pzip() function in src/pzip.c.
    The pzip() function involves creating pthreads, synchronizing them, and joining them to achieve parallel execution.
    Input and output data structures are provided and should not be modified.
  1.4 Assumptions
    The number of threads is assumed to be greater than or equal to one.
    The input file's characters are assumed to be a positive multiple of the number of threads.
    Each thread processes an equal portion of input characters.
    Consecutive occurrences of a character across threads should be reported separately.

  1.6 What I implemented:
    Implement the body of the pzip() function in src/pzip.c.
    Create a callback pthread function called by pthread_create() within pzip().
    Populate output pointers properly by the end of the pzip() function.
  1.7 Input File Format
    The input file contains only lowercase letters (a-z).
    Example: aaeeoooooeee
    Use provided script to generate inputs: ./generate_chars.py NUM > test_input
  1.8 Output Format
    Two output formats: Binary Output (default) and Text Output (--debug mode).
    Binary output is a file generated using zipped_chars array and zipped_chars_count.
    Text output (debug mode) displays character occurrences in human-readable text.
2. Evaluation 
  2.1 Grading
    Grading based on functionality, accuracy, parallelism, performance, and adherence to requirements.
    Performance measured using parallel efficiency (PE).



3. Resources
  Use pthread library calls: pthread_create, pthread_join, pthread_mutex_init, pthread_barrier_init, pthread_mutex_lock, pthread_mutex_unlock, pthread_barrier_wait.
  Refer to pthread tutorials for guidance.
