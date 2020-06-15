# James' Python Tutorial Exercises

## Intro

The aim of this tutorial is to facilitate trial-and-error learning, by setting you tasks you may or may not know how to complete. Some exercises may only take a few minutes to figure out, others may take a lot longer, because you are _figuring out_ the solution each time, not just following instructions. Hints are provided for tools you may wish to use and places you may find useful information, but the biggest hint of all is this: wing it.

Try anything and everything that occurs to you to get the desired outcome from your code, then run it to see if it works. If it doesn't work, try something else and run it again. Google any error messages you get and try out solutions. Even if you don't find someone with your exact problem, try looking for similarities and wiggling your code around a bit, change anything you think might be a common cause of the problem.

Run, run and run your code again. Python is quite a forgiving (easy to write) programming language which lends itself to a fast development cycle of coding iteratively: write code, run code, code fails, fix code, code works, write more code, code fails again, fix code again, rinse and repeat. This trial-and-error approach is a good way to learn what works and what doesn't, and develop your programmer's intuition.

### Using these tutorial files

1. Install `brew` using the terminal command
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
2. Install `git` using the terminal command
```
brew install git
```
3. Download the files in this tutorial with the terminal command
```
git clone https://github.com/jamcowl/PythonTutorial.git
```
This will create a folder called `PythonTutorial` with all the tutorial files in it. The file `sample2k.txt` contains the first 2000 rows of car crash data. It's a simple `.txt` (text) file, not a `.dta` file, so you won't need any fancy libraries to read it in Python. It only contains 5 columns. It looks like this:
```
latitude longitude HitRun year month timeofcrash
41.3378791809082 -73.08402252197266 0.0 2015.0 1.0 17:03:00
41.331729888916016 -73.07666778564453 0.0 2015.0 1.0 08:38:00
41.35139083862305 -73.06727600097656 0.0 2015.0 1.0 12:53:00
41.334938049316406 -73.08783721923828 0.0 2015.0 1.0 14:20:00
... etc ...
```

## Exercises Part A

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

Print just the first 2 items in each row (i.e. the latitude and longitudes only) to the screen.

Hint: take a look at [this documentation on Python lists](https://www.w3schools.com/python/python_lists.asp) to see how to pull out a specific item from a list.

### 8. Writing to a file

Print just the latitudes and longitudes from the data into a new file called `output8.txt`.

Hint: take a look at [the examples for Python's `write()` function](https://www.w3schools.com/python/python_file_write.asp).

### 9. If statements

Print just the latitudes and longitudes of carcrashes **which took place in February** into a new file called `output9.txt`.

Hint: you may wish to use [Python's `if()` command](https://www.w3schools.com/python/python_conditions.asp) and the date columns in the data.

## Exercises part B

### 10. String manipulation

Create a new file called `output10.txt` containing just the dates from the original sample, but in a more easily readable format, e.g. instead of `2015.0 2.0 12:02:00`, write `Feb-2015, 12:02` on each line.

Hint: create your own list of 12 strings, "Jan", "Feb" etc, and use the index of each month's position in the list. Use the `split()` method, like in exercise 6, but with "." or ":" as the separatro to separate different parts of the string.

### 11. Booleans

Use the values in the `HitRun` column to separate the data into 2 files: `output11_hitrun.txt` and `output11_nothitrun.txt`

Hint: you may have to create 2 different files for [Python's `write()` function](https://www.w3schools.com/python/ref_file_write.asp) to write to. You could do this in parallel (within a single `for` loop) or in series (2 `for` loops, one after the other). You may wish to convert the value of the `HitRun` column to a `bool` (a Boolean True/False value). See [here](https://kite.com/python/answers/how-to-convert-a-string-to-a-boolean-in-python) for further details.

### 999. Other exercises to come
