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

## Questions

### 1) ASCII Art

#### Print the following ASCII art:

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

### 2) Printing Integers
#### Print all integers (one per line) between 0 and 999,999 (do not include 0 or 999,999) that have the same first and last digit, and are divisible by 3, 5, or 7.

- Sample output:
```
3
5
7
9
33
...

```

### 3) k-th largest
#### Given a list of numbers and an `k` such that `1 <= k <= length of list`, find the kth largest unique element. 
- Note the list may not be sorted and may have duplicates.

- Input format:
```
T           # number of test cases
L           # list of numbers with spaces in between
k           # k
```

- Example input:
```
1                  # 1 test case
0 3 6 2 4 3 3 7 6  # list of numbers
5                  # k
```
- Example output:
```
2
```

- Example input:
```
2                             # 2 test cases
3.14159 -1000 999999999 3.14  # list
3                             # k
0 0 0 0 0 0 1 -1 0 0 0 0 0 0  # list
2                             # k
```
- Example output:
```
3.14
0
```

### 4) Unique names
#### Given a list of names, print the longest set of names in which no name shares a character with any other name in the set at the same index. You can ignore case.

- Input format:
```
T         # number of test cases
L         # list of names separated by spaces
```
- Output format:
```
Name1 Name2 Name3 Name4          # List corresponding to the first test case
OtherName1 OtherName2 OtherName3 # List corresponding to the second test case
...
```

- Example input:
```
1                # one test case
Dan Dylan Wyatt  #
```
- Example output:
```
Dan Wyatt        #  Dan and Dylan both have 'd' at index 0, and Dylan and Wyatt both have 'y' at index 1, so {Dan, Wyatt} is the largest set that does not share characters at the same vertex
```

### 5) CS Universities
#### Print the names of all universities in the United States (1 per line and no abbreviations) that have at least 7,000 undergraduate students and offer Computer Science majors.

### 6) Largest Convex Polygon
#### Given a list of coordinate pairs, return the longest sequence of points that can be connected in a loop, without any of the connecting lines intersecting, and such that the resulting polygon is convex. Give the output in clockwise order.

- Input format:
```
T                     # number of test cases
x1 y1 x2 y2 x3 y3 ... # list of coordinates
...
```
- Output format:
```
x1 y1 x2 y2 x3 y3 ... # list of coordinates for test case 1
x1 y1 x2 y2 x3 y3 ... # list of coordinates for test case 2
...
```

- Example input:
```
1
0 0 0 1 1 1 1 0 0 1 2 2 1
```
- Example output:
```
0 0 0 1 1 2 2 1 1 0
```
