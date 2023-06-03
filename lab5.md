# Lab Report 5
## Part 1 - Debugging Scenario
### 1. The original post from a student with a screenshot showing a symptom and a description of a guess at the bug/some sense of what the failure-inducing input is. (Don’t actually make the post; just write the content that would go in such a post)
### ![Image](edstem1.png)
### ![Image](edstem2.png)
### ![Image](edstem3.png)
Note: This is not code that I've written. I only added a bug for the purpose of this lab. In the write-up, it says, "Feel free to set this up by cloning and breaking some existing code like the grading script or code from class" so I am using the code from Week 9 Lab Scenario 2 (with the initial bug fixed).
### 2. A response from a TA asking a leading question or suggesting a command to try (To be clear, you are mimicking a TA here.)
"Good question. You said that your code 'seems to finish after line 10'. Think about a command you wrote in grade.sh that tells bash to exit when an error is encountered. Without turning this off, your code will immediately exit when it reaches a nonzero status. Since the error seems to be happening after cloning, what does that say about the location of the error? That might be where you want to turn something off. Refer to part 4 of the Your Grading Script Lab Task. Try to follow the suggestion it provides and see if that makes any difference."
### 3. Another screenshot/terminal output showing what information the student got from trying that, and a clear description of what the bug is.
### ![Image](not_buggy.png)
The screenshot above shows the changes the student made from listening and trying out the suggestion made by the TA, and the output that followed. The bug here isn't an error message like usual. Instead, the student was expecting to see two failures in the output, but because they added in ```set -e```, their code would exit before it ever got to doing that. The student attempted to turn this off in line 21 (before the bug was fixed), but it was in the wrong location, therefore bash would still exit even when it wasn't supposed to.
### 4. At the end, all the information needed about the setup including:
#### * The file & directory structure needed
#### ![Image](needed.png)
#### * The contents of each file before fixing the bug
#### ![Image](before1.png)
#### ![Image](before2.png)
#### ![Image](before3.png)
#### ![Image](before4.png)
#### ![Image](before5.png)
#### ![Image](before6.png)
#### ![Image](before7.png)
#### * The full command line (or lines) you ran to trigger the bug
```bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-lab3```
#### * A description of what to edit to fix the bug
Turn off ```set -e``` by taking what was originally in line 21 (```set +e```) and move it to before the line that has ```cp student-submission/ListExamples.java ./```.
## Part 2 - Reflection
Some things I learned from my lab experience in the second half of this quarter that I didn't know before are vim and how Gradescope tests are written. I understood that bash allowed multiple steps to happen such as compiling and then running, but I learned that it's able to do so much more than that and makes autograding possible. I assumed that these autograders were made in .java files and not .sh files. There are still many things that I still can learn about bash, but I certainly know more about it than I did earlier in the quarter. Vim was another thing I learned. Going through the tutorial was very interesting and let me explore this new thing in a fun way. There is so much that can be done from the command line that I didn't know about in the past until I took the labs in the second half of this quarter. This lab report is also a reflection of what I learned, as I didn't end up making a successful grading script, and one of the reasons why was because I was not using the ```set -e``` properly and I didn't understand the instructions for it very well. While the bug I created for this lab may not have created a typical error message, it was a bug that I made myself, so I thought it would be better to show than a bug I can easily point out. 
