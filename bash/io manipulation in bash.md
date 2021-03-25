Programs have default input and output streams.

## io manipulation using angled brackets `<` `>`
```bash
$ program < file
```
The above script tells Terminal to rewire the input of the program to be the output of the file.

```bash
$ program > file
```
This script tells Terminal to rewire the output of the program to be the input of the file and rewrite its contents.

```bash
$ program >> file
```
This script tells Terminal to rewire the output of the program to be the input of the file and append it to the end.

## io manipulation using pipe `|`
```bash
$ program1 | program2
```
i.e. Take the output of program1 and feed it as input to program2.

#### Example1
```bash
$ ls -l / | tail -n1
```
This uses the program `ls` to produce an output of a list of all files and directories in the root directory `/` and feed it as the input for program `tail` which then outputs the very last line of this input.

#### Example2
```bash
$ ls -l / | tail -n1 > ls.txt
```
This takes the output from Example1 and feeds it as input to a file, and hence creating a file named `ls.txt` with the programs output as its content.

## References
[Lecture 1: Course Overview + The Shell (2020)](https://www.youtube.com/watch?v=Z56Jmr9Z34Q&ab_channel=MissingSemester)
