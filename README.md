*This project has been created as part of the 42 curriculum by <`rhlou`>*
--
**-Description:**

Get Next Line is a C project that implements a function to read a file descriptor line by line, returning each line on successive calls. The goal of this project is to:

 .Practice dynamic memory management (`malloc`, `free`)

 .Handle multiple file descriptors simultaneously

 .Understand how the read() system call works and how to manage partial reads

 .Develop robust string manipulation functions and algorithms for reading efficiently

**-Instructions:**
---
compilation:
        Compile the project using:

        cc -Wall -Wextra -Werror main.c get_next_line.c get_next_line_utils.c 

# Execution:
    Run the program with files
        <./a.out>
---

**-Resources:**

    youtube tutorial : 
    "https://youtu.be/jT9N8gY36Os?si=lB2YGKipjUTMV9Co" .(general idea about the path of the algorithme and basic infos about open , read , static variabels)
    peer to peer learning .(help in the bonus and protecting the code from flows ..)
    Documantd : "https://www.geeksforgeeks.org/c/input-output-system-calls-c-create-open-close-read-write/" .(understand the file descriptors)
---

**-Algorithm Explanation:**

The Get Next Line function reads a file descriptor line by line. It works by storing leftover data in a stash between function calls. On each call:

1.Data is read from the file descriptor into a temporary buffer until a newline is found or EOF is reached.

2.A line is extracted from the stash, including the newline if present, and returned.

3.The stash is updated to keep any remaining data for the next call.

For the bonus part, a separate stash is maintained for each file descriptor, allowing multiple files or streams to be read simultaneously without interfering with each other.

This approach ensures efficient memory use, handles partial reads and multiple newlines, and works correctly for both single and multiple file descriptors.
# get_next_line
