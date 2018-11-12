# VandyApps Code Golf Fall 2018

### Overview
This competition focuses on short and succinct code. 
The challenge is to produce answers to the provided problems with as little code as possible.
Your score for each problem will be the file size of your source code for that problem. Your code will not be run. We will assume that your code runs. We will verify the answers your code produces.
However, we will have the 1st, 2nd, and 3rd place contestants run their code live for proof that
it runs and proof that it produces the correct output. Submission input will be released 10 minutes before the end of the competition; example input is supplied in each problem description.
* **The actual code you submit cannot be generated text**
* Your code cannot call any external processes
* Your code must be able to be run independently of any other personal files (i. e. you can use standard libraries and other modules but you can't write code in another file and simply call it in your submission file)

### Submission
You will need to submit the source code for each question.
Fork this GitHub repository, and just copy and paste your repository link [here](https://goo.gl/forms/qTg8xoZpNKi86IWB3)
* Each _solution_ file (your actual code) must be in a directory titled `solutions`
* Generate _answer_ files using your solution. The input files are in the `inputs` directory. Each individual input is separated by a newline. Separate your output in the file by newlines.
* Each _answer_ file (your generated answers) must be in a directory titled `answers`
* Each file must have the problem number somewhere in its name
* You should only submit the files we have asked for and nothing else
* There should be no dots ("." charachters) in your filename except before the extension
* The file size of your file will be evaluated with the python function [os.path.getzise](https://docs.python.org/2/library/os.path.html?highlight=os.path.getsize#os.path.getsize) on an Ubuntu OS. Make sure this is not problematic for your source code.
* **you cannot compress your files** you must submit your raw source code

#### Sample Valid Solution Filenames:
* prob_1.py
* prob1.py
* 1.java
* jibberish1jibberish.cpp

#### Sample Invalid Solution Filenames:
* i_dont_contain_a_number.py
* x.java
* get.ridOfThatExtraDot.cpp
* .filename.java

#### Sample Valid Answer Filenames:
* prob_1_out.txt
* prob1.txt
* 1.txt
* whatever1whatever.txt

#### Sample Invalid Answer Filenames:
* i_dont_contain_a_number.py
* x.txt
* get.ridOfThatExtraDot.cpp
* .filename.txt

### Questions

#### 1) ASCII Art

Print the following ASCII art:

```ascii
 / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \_
/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \__
\ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / _
 \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ / 
 / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \_
/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \__
\ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / _
 \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ / 
 / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \_
/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \__
\ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / _
 \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ / 
 / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \_
/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \__
\ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / _
 \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ / 
 / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \_
/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \__
\ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / _
 \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ / 
 / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \__/ / __ \ \_
/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \____/ /  \ \__
```

#### 2) Given a grid of 0's and 1's, count the number of 1's between the rectangle formed by the given coordinates
- Coordinates are 0 based indices and inclusive
- *Warning*: the grid can be large
- Example input
```
R C               # length of the rows and columns of the grid
N                 # number of test cases
X_1 Y_1 X_2 Y_2   # coordinates per test case
...
```
```
5 12
0 1 0 0 0 1 0 1 1 0 0 0
0 0 0 0 0 1 0 0 1 0 1 1
0 1 0 0 0 1 1 1 1 1 1 0
0 1 0 0 0 1 0 0 0 1 0 1
1 0 0 1 1 0 0 0 1 0 0 0
3
0 0 4 11
0 1 4 1
0 1 2 5
```

- Example output:
```
23
3
5
```

#### 3) Today, the Alumni Association tabled at Sarratt Promenade and gave out Chick-Fil-A sandwiches "while supplies last"ed. Fortunately, before the event we discovered how many sandwiches were ordered. Given the order in which students arrived, we want to know how long the line is at a certain time and how many sandiwches are left at that time.

- Additional specifications
    - It is not possible to receive a sandwich until after interacting with someone from the Alumni Association. Since the time spent talking to someone from the Alumni Association is related to a student's year, the following are interaction times for each class.
        - 1 (Freshman):     1 minute
        - 2 (Sophomore):    2 minutes
        - 3 (Junior):       4 minutes
        - 4 (Senior):       9 minutes
    - Once sandwiches run out, all students leave the line.
    - Time starts at 0

- Input format:
```
T               # number of test cases
C               # count of sandwiches
S               # number of students
t_i class       # S lines of time and class
I               # Output line length and remaining sandwich count at time I
```

- Example input:
```
1               # 1 test case
1               # 1 sandwich
1               # 1 student
0 1             # Student comes at t=0 and class = 1 (freshman)
0               # Time to output
```
- Example output:
``` 
1 1            # The line is 1 minute long and there is 1 sandwich at time 0
```

- Example input:
```
2               # 2 sets of test cases
5               # 1st TC
3             
1 1
2 2
3 4
3               # Print line length & sandwich count at t=3
1               # 2nd TC
3
4 2
6 2
7 3
8               # Print line length & sandwich count at t=8
```
- Example output:
```
10 4            # 10 minute long line and 4 sandwiches remaining (A student received a sandwich after t=1, and 2 more in line)
3 1             # One received a sandwich after t=5, one received a sandwich after t=7, last person has been in line for 1 minute
```

Plug
```
With VUconnect, you can:
·         Network with over 135,000 alumni worldwide
·         Get alumni advice for internships, jobs, and graduate school
·         Access the Alumni Career Adviser Network
·         Find Alumni Chapters - to network in your hometown/where you'd like to move after graduation
 
```

