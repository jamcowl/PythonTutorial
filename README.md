# James' Python Tutorial Exercises

## Intro

The file `sample2k.txt` contains the first 2000 rows of car crash data. It's a simple `.txt` (text) file, not a `.dta` file, so you won't need any fancy libraries to read it in Python. It only contains 5 columns. It looks like this:
```
latitude longitude HitRun year month timeofcrash
41.3378791809082 -73.08402252197266 0.0 2015.0 1.0 17:03:00
41.331729888916016 -73.07666778564453 0.0 2015.0 1.0 08:38:00
41.35139083862305 -73.06727600097656 0.0 2015.0 1.0 12:53:00
41.334938049316406 -73.08783721923828 0.0 2015.0 1.0 14:20:00
... etc ...
```
You can download the files in this tutorial with the command
```
git clone https://github.com/jamcowl/PythonTutorial.git
```
This will create a folder called `PythonTutorial` with all the tutorial files in it.

## Exercises

### 0. Running a Python script
Write a Python script called `mycode.py` which can print the words "Hello World" to the screen.

Hint: use Python's [`print()` function](https://www.w3schools.com/python/ref_func_print.asp).

### 1. Reading a file
Read the data file `sample2k.txt` and print the first few rows to the screen.

Hint: use Python's [`open()` and `readline()` functions](https://www.w3schools.com/python/ref_file_readline.asp).

### 2. For loops
Develop your solution to question 1 using a for loop to print every row to the screen.

Hint: take a look at the answers to [this StackExchange question](https://stackoverflow.com/questions/17949508/python-read-all-text-file-lines-in-loop).

### 3. For loops with indexed numbers
Change your `for` loop to track which row number each line of the file is.

Hint: take a look at [this explanation of the `enumerate()` function](https://treyhunner.com/2016/04/how-to-loop-with-indexes-in-python/#enumerate).

### 4. Printing row numbers

Change your `for` loop to print the row number next to each line of the file.

Hint: see [here](https://www.w3schools.com/python/gloss_python_string_concatenation.asp) to learn about concatenating strings in Python and look at [the `str()` function](https://www.w3schools.com/python/gloss_python_string_concatenation.asp) in case you need to combine strings and numbers.

### 5. Comments

Use the `#` character at the start of some lines in your `for` loop to comment out the printing lines, so that your screen is not filled with loads of output when you run your code.

Hint: use `print()` to add some messages before and after your code so that when you run it, you can see what stage it's at.

### 6. Splitting strings

Instead of printing each line of the file as one long string, split it into a list of individual strings.

Hint: you can use [the `split()` function](https://www.w3schools.com/python/ref_string_split.asp) to split a long string into a list of strings.

### 7. Lists

Print just the first item in each row (i.e. the latitude only) to the screen.

Hint: take a look at [this documentation on Python lists](https://www.w3schools.com/python/python_lists.asp) to see how to pull out a specific item from a list.

### 999. Other exercises to come
