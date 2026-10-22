## Task

Today’s goal is **NOT to write code**.

Today you will learn **how to think before writing automation code**.

Instead of directly opening VS Code and writing Python, you will:
- Pick **one script** you already wrote (Day 01 to Day 06)
- Understand what problem that script is solving
- Write down:
  - What is the problem?
  - What input does it need?
  - What output should it give?
  - What steps are involved?

This day is about **clear thinking**, not coding.

## DAY 6 : Argparser ( CLI Tool for DevOps )
  - What is the problem?
    If there is a log file or any report file where in we need to find out the number of occurance of a particular event of any file ,
    instead of manually counting the number of occurance, automating the whole process of providing the file and mentioning the desired keyword
    directly via CLI , saves much time and effort .
    
  - What input does it need?
    It takes the following inputs:
    - --input  : the file which needs to be parsed is required to pass here along with the ' --input ' flag
    - --keyword: which particular word are we looking for / occurance of the word in the given file ; required to pass here with ' --keyword ' flag
    - --output : name of the file , where we want the result to be saved into ( a new file will be generated at the location were the logfile is stored );
                  pass with ' --output ' keyword

  - What output should it give?
    This gives out a new file mentioning the number of occurance of the keyword in the log file .

  - What steps are involved?
    
    Step 1:
    
    if __name == '__main__'
    This step makes sure , if the same file was executed directly.

    Step 2:
    
    import argparse
    and mention the flags required as inputs from the user while running the script; by instatiating the argumentparser object

    Step 3:
    - convert the CLI arguments to accessible python attributes using :
      args = parser.parse_args()

    - store the specific keyword from CLI argument to a variable which needs to be parsed in the logfile using:
      key = args.keyword

    - initialise the word_count = 0  

    Step 4:
    
    Open the inputs as a file in read 'r' mode and iterate through the lines for the keyword passed in the CLI arguments & add it to the word_count

    Step 5:
    
    Save the word_count generating the file mentioned in the CLI argument as --output and print the same to the terminal as a success message with file name.
      


