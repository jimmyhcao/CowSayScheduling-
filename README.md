<h1>Cow Say 🐮 Scheduling</h1>


<h2>Description</h2>
Monitoring employee schedules is essential for optimizing workforce management, maintaining compliance, enhancing productivity, ensuring customer satisfaction, and promoting a positive work environment. It helps strike a balance between the needs of the business and the well-being of its employees.

<br> For this project, I was hired by Lucky Duck Casino in the capacity of a Security Analyst. My role involved developing a shell script designed to efficiently analyze employee schedules. The purpose of this script is to aid in identifying the employee on duty during specific times, particularly in situations involving future losses or incidents. 

<h4>Operating System:</h4>
<li>Linux</li>

<h4>Commads:</h4>
<li>grep
  <li>awk
  <li>cowsay</li>

<h2>Command Basics</h2>
<h4>grep</h4>
<b>'grep'</b> is a command-line utility in Unix and Unix-like operating systems used for searching and matching patterns within text files. It stands for "Global Regular Expression Print." grep allows you to search for lines in files that match a specified pattern or regular expression and then print those lines to the terminal or redirect the output to another file.

<br>Here's a basic usage of 'grep':

```
grep pattern filename
```
<i>Where:</i>
<li> <b>'pattern'</b> is the regular expression or text string you want to search for.
<li> <b>'filename'</b> is the name of the file(s) you want to search in.</li>

For instance, to search for all lines containing the word "example" in a file called file.txt, you would use:
```
grep example file.txt
```

<br>grep provides various options and flags for more advanced text searching and manipulation. Some common options include:

<b>-i</b>: Ignore case (perform case-insensitive matching).
<br><b>-r</b> or <b>-R</b>: Recursively search directories.
<br><b>-l</b>: Display only the names of files containing the pattern.
<br><b>-v</b>: Invert the match (display lines that do not match).
<br><b>-n</b>: Display line numbers along with matching lines.
<br><b>-c</b>: Count the number of matches instead of displaying lines.

<br> A full list and description of the grep options and flags can be viewed by running <b>'man grep'</b> in the terminal
