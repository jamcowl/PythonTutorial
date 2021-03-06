# James' Python Tutorial Exercises

## Intro

<details><summary>Click to expand</summary>
<p>
  
The aim of this tutorial is to facilitate trial-and-error learning, by setting you tasks you may or may not know how to complete. Some exercises may only take a few minutes to figure out, others may take a lot longer, because you are _figuring out_ the solution each time, not just following instructions. Hints are provided for tools you may wish to use and places you may find useful information, but the biggest hint of all is this: wing it.

Try anything and everything that occurs to you to get the desired outcome from your code, then run it to see if it works. If it doesn't work, try something else and run it again. Google any error messages you get and try out solutions. Even if you don't find someone with your exact problem, try looking for similarities and wiggling your code around a bit, change anything you think might be a common cause of the problem.

Run, run and run your code again. Python is quite a forgiving (easy to write) programming language which lends itself to a fast development cycle of coding iteratively: write code, run code, code fails, fix code, code works, write more code, code fails again, fix code again, rinse and repeat. This trial-and-error approach is a good way to learn what works and what doesn't, and develop your programmer's intuition.

</p>
</details>

## Using these tutorial files
<details><summary>Click to expand</summary>
<p>

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
</p>
</details>

## Exercises part A

<details><summary>Click to expand</summary>
<p>

### 0. Running a Python script
Write a Python script called `mycode.py` which can print the words "Hello World" to the screen.

Hint: use Python's [`print()` function](https://www.w3schools.com/python/ref_func_print.asp).

### 1. Reading a file
Read the data file `sample2k.txt` and print the first few rows to the screen.

Hint: use Python's [`open()` and `readline()` functions](https://www.w3schools.com/python/ref_file_readline.asp).

### 2. For loops
Develop your solution to question 1 using a `for` loop to print every row to the screen.

Hint: take a look at the answers to [this StackExchange question](https://stackoverflow.com/questions/17949508/python-read-all-text-file-lines-in-loop).

### 3. For loops with indexed numbers
Change your `for` loop to track which row number each line of the file is.

Hint: take a look at [this explanation of the `enumerate()` function](https://book.pythontips.com/en/latest/enumerate.html).

### 4. Printing row numbers

Add code within your `for` loop to print the row number next to each line of the file.

Hint: see [here](https://www.w3schools.com/python/gloss_python_string_concatenation.asp) to learn about concatenating strings in Python and look at [the `str()` function](https://www.w3schools.com/python/gloss_python_string_concatenation.asp) in case you need to combine strings and numbers.

### 5. Comments

Use the `#` character at the start of some lines in your code to "comment out" code that you don't want any more, e.g. so that your screen is not filled with loads of output when you run your code.

Hint: use `print()` to add some messages throughout your code so that when you run it, you can see what stage it's currently at.

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

Print the row number and a statement on whether the crash "was in February" or "was NOT in February" to the screen, for every row in the data.

Hint: you may wish to use [Python's `if()` command](https://www.w3schools.com/python/python_conditions.asp) and the date columns in the data.

</p>
</details>

## Exercises part B

<details><summary>Click to expand</summary>
<p>

### 10. String manipulation

Create a new file called `output10.txt` containing just the dates from the original sample, but in a more easily readable format, e.g. instead of `2015.0 2.0 12:02:00`, write `Feb 2015, 12:02` on each line.

Hint: you way wish to create your own [list](https://www.w3schools.com/python/python_lists.asp) of 12 strings, "Jan", "Feb" etc, and use the index of each month's position in the list. You may also wish to use the `split()` method, like in exercise 6, but with "." or ":" as the separator to separate different parts of the string.

### 11. Booleans

Use the values in the `HitRun` column to separate the data into 2 files: `output11_hitrun.txt` and `output11_nothitrun.txt`, which contain the full row of data from crashes which were and were not "hit & run" crashes, respectively. Make sure that both files have column headings.

Hint: you may have to use [Python's `write()` function](https://www.w3schools.com/python/ref_file_write.asp) twice with 2 different filenames. You could do this in parallel (within a single `for` loop) or in series (2 `for` loops, one after the other). You may wish to convert the value of the `HitRun` column to a `bool` (a Boolean True/False value). See [here](https://kite.com/python/answers/how-to-convert-a-string-to-a-boolean-in-python) for further details. You may have to use an `if()` statement to try and treat the first row (which has column headings) differently to the others.

### 12. Dictionaries

Read in all the car crash data and store it in a dictionary, by human-readable month (i.e. the "keys" will be strings like "Feb 2015"). The "value" should be a list of car crashes which occurred that month. You should store a list of boolean `True`/`False` values to represent each crash as either a hit & run or not a hit & run. Print this dictionary to the screen. Finally, for each month, print statements in the form `"In February 2015, there were 30 crashes of which 12 were hit & run incidents"` to the screen.

Hint: you will have to use [Python's `dict` type](https://www.w3schools.com/python/python_dictionaries.asp) as well as the [lists](https://www.w3schools.com/python/python_lists.asp) you have already been using. You may find it effective to create an empty list for each month, then add the booleans to it with [the `append()` function](https://www.programiz.com/python-programming/methods/list/append). Finally, [the `len()` function](https://www.w3schools.com/python/ref_func_len.asp) or the answers to [this StackExchange question](https://stackoverflow.com/questions/2643850/what-is-a-good-way-to-do-countif-in-python) may help when counting the totals at the end.

### 13. Dictionaries 2: Electric Boogaloop

- Store all the car crash data in a dictionary with hit & run booleans as before, but instead of a month, use the time of day (down to the minute) as the key. Your dictionary should **not** contain redundant times when no crashes occured.

- Are there any times with more than 1 crash recorded? Print those times to the screen.

- Print a list of times with no crashes (i.e. times, down to the minute, which do *not* appear in the data) to the screen.

- Using only your existing dictionary (i.e. without reading the sample file again) create a second dictionary where the value stored for each time is a single value: the fraction of "hit & run" crashes recorded at that time of day.

- Sort your dictionary by "hit & run" fraction and print the top 10 worst times to the screen.

Hint: there are only 60 × 24 = 1440 minutes in a day, so with 2000 crashes non-uniformly distributed, there will inevitably be some overlap, but also likely some minutes with no recorded crashes at all. You may wish to start with an empty `dict` and dynamically [add entries to it](https://www.journaldev.com/23232/python-add-to-dictionary) as you read in the data line by line. You may need an `if()` statement to [check if that time already exists in the `dict`](https://able.bio/rhett/check-if-a-key-exists-in-a-python-dictionary--73iajoz). Note that [you can iterate over a `dict` using a `for` loop](https://mkyong.com/python/python-how-to-loop-a-dictionary/) in much the same way as a list. You can also [sort a `dict` by key or by value](https://www.pythoncentral.io/how-to-sort-python-dictionaries-by-key-or-value/).

### 14. Functions

- Write a function called `listFromFileName()` which takes as its argument a filename and returns a `list` of strings, with 1 string per line of the input file.

- Print the 1st, 2nd, 10th and 100th elements from this list to the screen.

- Create a second function called `dictFromList()` which can take a `list` of strings (in the form defined above) as its argument and `return` a `dict` where the keys are nice month strings (e.g. "Feb 2015") and the values are a list of `[latitude,longitude]` pairs representing the location of each car crash occuring in that month (i.e. this will be a list of 2-element lists).

- Create a third function `countCrashes()` which takes two arguments: first, a `dict` (in the form defined above) and second, a string naming a month and year (e.g. "Feb 2015"). This function should read the `dict`, look for the supplied month, count how many crashes happened in that month, and return a single `int` total number of crashes.

- Improve the `countCrashes()` function with an `if()` statement at the beginning, which will check whether the requested month exists in the supplied `dict` or not. If it does not, you should `print()` an error message of your choice to the screen, then the function should `return` a value of `-1`.

- Test these functions by running the following code.
```
# get dict from filename
crashDict = dictFromList(listFromFileName("sample2k.txt"))

# how many crashes in Feb 2015?
nFeb2015 = countCrashes(crashDict,"Feb 2015")
print("Number of crashes in Feb 2015 = "+str(nFeb2015))

# do we have data on the future?
nOct2030 = countCrashes(crashDict,"Oct 2030")
print("Number of crashes in Feb 2015 = "+str(nOct2030))
```

Hint: look at [these examples](https://www.w3schools.com/python/python_functions.asp) for how to define a function with 1 or more input arguments in Python.

Note: it is a common tendency to make functions that `return` a value of `-1` if they encounter an error, rather than not returning a value at all, or quitting the program entirely. This enables other parts of a program that use a function to have contingencies built in for when something strange happens.

### 15. Modules

* Create a new file, `myTools.py`, containing just the 3 functions you defined in exercise 14 (`listFromFileName()`,`dictFromList()` and `countCrashes()`).

* Create a second new file `simpleTest.py` and copy across _just_ the test code from exercise 14. Do **not** copy across your function definitions. Instead, `import` your new module `myTools` at the top of the file and insert a `myTools.` prefix before the function names. What happens when you run this new `simpleTest.py` code? What if you comment out the `import` line at the top?

Hint: look at [this documentation](https://www.w3schools.com/python/python_modules.asp) on how to use modules in Python.

Protip: you can actually get around using the `myTools.` prefix by using an `import` command of the form `from myTools import *` instead. However, when using multiple modules in a more elaborate program, it can be helpful to keep the named source of each imported function/variable explicit in your code so you can keep track of dependencies.

Bug alert: if you have trouble running newly created code files, the problem may be with permissions. Try the terminal command e.g. `chmod 755 someNewPythonFile.py` to fix this.

</p>
</details>

## Exercises part C

### 16. Plotting

* Create a bar graph with the name of the month on the x-axis, and the total number of crashes for each month on the y-axis.

* Create a second, stacked bar graph, showing the hit-and-run crashes on top of the crashes that were not hit-and-runs.

Hint: look at [this documentation](https://matplotlib.org/3.1.1/gallery/lines_bars_and_markers/bar_stacked.html) on how to make stacked bar graphs. You should be able to use a line similar to the first `bar()` to create a regular (non-stacked) bar graph as well. You may first need to install the `matplotlib` module, which you can find instructions for [here](https://matplotlib.org/3.2.2/users/installing.html#installing-an-official-release). 

Plot function [here](https://matplotlib.org/3.2.2/api/_as_gen/matplotlib.pyplot.plot.html)
