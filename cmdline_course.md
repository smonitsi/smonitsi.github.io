---
layout: default
---

## What is it?

In fall 2025 I took the course [Command-line tools for linguists](https://studies.helsinki.fi/kurssit/opintojakso/otm-92ee484e-456b-409f-a397-d9d2b6e40a2f/KIK-LG221) in University of Helsinki to learn the basics of command-line tools. Because the course was aimed for linguists, one of its main focuses was in text-editing. The course was divided into four modules with different learning goals. 

### Module 1: Introduction to Command Line Environments

On the first module I learned the very basics of UNIX commands, including
- navigating directories
- creating and removing files and directories
- copying and moving files and directories
- change the read and write permissions for files

Example of the code I wrote for navigating directories
```
mkdir KIK-LG221
cd KIK-LG221
mkdir week1
cd week1
mkdir homework1
cd homework1
pwd
```
 
### Module 2: Text Processing in UNIX

On the second module I learned more advanced UNIX commands for text processing, including
- converting text files
- sorting textfiles using sort and uniq
- finding patterns using grep, sed and RegEX
- how to pipe commands

Here's a code I wrote for creating a frequency list from textfile to find most frequent words:

```
cat some_textfile.txt | tr -s '\n\r\t ' '\n' | tr -dc "A-Za-z0-9\n'" | sort | uniq -c | sort -n
```


### Module 3: Scripting, Configuration Files and Installing Programs


On the third module I learned how to write bash scripts and how to install files using brew and pip. I learned how to use if -command and utilize loops in text processing.

Here's a script I wrote for simple word conjugation in English. The program takes a line from a text file, ideally a list of adjectives, and turns them in comparative form. It works for regular cases and words ending with y.
```
#!/bin/bash

while read -r line; do
  if [ "${line: -1}" = "y" ];
  then
    echo $line"er" | sed "s/yer$/ier/g" 
  else
    echo $line"er"
  fi
done < $1
```

### Module 4:

The fourth module focused on learning version control by using Github. I learned how to add, commit and push changes from local repository to remote repository. I also practiced using different branches to test code and how to merch branches. This site is created by using Github and is the final project of the course. I also learned how to use Markdown to format the site.

With Markdown I could, for example, create a table like this:
```
| Animals       | Striped       | Do I like them  |
| ------------- |:-------------:| ---------------:|
| Bees	        | Yes		| They are ok     |
| Giraffes      | No	        | Very much yes   |
| Okapis	| Yes	     	| Absolutely yes  |
| Seahorses	| Some are	| Mostly yes      |
| Wasps		| Yes		| **NO**	  |
| Zebras	| Yes		| Absolutely yes  |
```
And it would look like this:

| Animals       | Striped       | Do I like them  |
| ------------- |:-------------:| ---------------:|
| Bees	        | Yes		| They are ok     |
| Giraffes      | No	        | Very much yes   |
| Okapis	| Yes	     	| Absolutely yes  |
| Seahorses	| Some are	| Mostly yes      |
| Wasps		| Yes		| **NO**	  |
| Zebras	| Yes		| Absolutely yes  |

___

### End reflection

After the course I feel more comfortable in my programming skills. I found the text processing tools useful for my future projects and career development. Creating websites is something I've wanted to learn for a long time and I'm happy to have completed this final project and hope to develop my skills more in the future.

![Thank you](https://www.publicdomainpictures.net/pictures/230000/t2/thank-you-lobster-text-title.jpg)