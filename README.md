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
<h3>grep</h3>
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

<br> A full list and description of the grep options and flags can be viewed by running <b>'man grep'</b> in the terminal.
<hr>
<h3>awk</h3>
The <b>'awk'</b> command is a versatile text-processing tool in Unix and Unix-like operating systems. It is often used for processing and manipulating structured text data, such as log files, CSV files, and configuration files. awk allows you to define patterns and actions to perform on each line of input, making it a powerful tool for tasks like data extraction, transformation, and reporting.

<br>The basic syntax of the 'awk' command is as follows:
```
awk 'pattern { action }' filename
```
<i>Where:</i>
<li> <b>'pattern'</b> is a condition that specifies which lines to apply the action to.
<li> <b>'action'</b> is a set of commands to be executed on lines that match the pattern.
<li> <b>'filename'</b> is the name of the file you want to process. If you don't specify a filename, awk reads from standard input (e.g., the output of another command or data piped into it).</li>

<br>For example, the awk command can be configured to print specific columns from a CSV file (or any delimited file) using the following flags:
```
awk -F',' '{print $1, $3}' data.csv
```
<i>Where:</i>
The command uses a comma as the field separator (-F',') and prints the first and third columns from the file data.csv.

<br>There are many other use cases for the awk command. A full listing of commands and flags can be viewed by running <b>'man awk'</b> in the terminal.

<hr> 
<h3>cowsay</h3>
<b>cowsay</b> is a famous command line program loved by many programmers that generates ASCII art of an animal (usually a cow) along with a speech bubble containing text that you provide. It's often used for entertainment or to add a touch of humor to command-line interactions.

<br>cowsay will need to be installed before operating, using the following commands:
```
brew install cowsay
sudo apt-get install cowsay
yum install cowsay
```

To use cowsay, you typically follow this syntax:
```
cowsay [options] [your_text]
```
<i>Where:</i>
<li> <b>'options'</b>: Optional flags that modify the appearance or behavior of the cow or text.
<li> <b>'your_text'</b>: The text you want the cow to say in the speech bubble.</li>

<br>For example, if you were to run "cowsay <b>"Hello, world!"</b>, the output woud look something like this:
```
 _______
< Hello, world! >
 -------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```















