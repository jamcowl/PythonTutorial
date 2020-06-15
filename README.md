# James' Python Tutorial Exercises

## Intro

The file `sample2k.txt` contains the first 2000 rows of car crash data. It's a simple `.txt` (text) file, not a `.dta` file, so you won't need any fancy libraries to read it in Python. It looks like this:
```
latitude longitude HitRun year month timeofcrash
41.3378791809082 -73.08402252197266 0.0 2015.0 1.0 17:03:00
41.331729888916016 -73.07666778564453 0.0 2015.0 1.0 08:38:00
41.35139083862305 -73.06727600097656 0.0 2015.0 1.0 12:53:00
41.334938049316406 -73.08783721923828 0.0 2015.0 1.0 14:20:00
... etc ...
```
You can download the files in this tutorial to a folder on your MacBook with the command
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

Hint: take a look at the answers to [this StackExchange question](https://stackoverflow.com/questions/17949508/python-read-all-text-file-lines-in-loop))

3. 



Use the `#` character at the start of some lines in your `for` loop to comment out the printing lines, so that your screen is not filled with loads of output when you run your code. Use `print()` to add some messages before and after your code so that when you run it, you can see what stage it's at.

