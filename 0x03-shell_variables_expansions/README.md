0. 
Write a script that prints “Hello, World”, followed by a new line to the standard output.
echo -e "Hello, World"

1.
Write a script that displays a confused smiley "(Ôo)'.
echo "\"(Ôo)'"

2.
Display the content of the /etc/passwd file.
cat /etc/passwd

3.
Display the content of /etc/passwd and /etc/hosts
cat /etc/passwd /etc/hosts

4.
Display the last 10 lines of /etc/passwd
tail /etc/passwd

5.
Display the first 10 lines of /etc/passwd
head /etc/passwd

6.
Write a script that displays the third line of the file iacta.
head -n3 iacta | tail -1

7.
Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.
ls -la > ls_cwd_content

8.
Write a shell script that creates a file named exactly \*\\'"Holberton School"\'\\*$\?\*\*\*\*\*:) containing the text Holberton School ending by a new line.
echo 'Holberton School' > '\*\\'\''"Holberton School"\'\''\\*$\?\*\*\*\*\*:)'

9.
Write a script that duplicates the last line of the file iacta
tail -n1 iacta >> iacta

10.
Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.
find . -type f -name '*.js' -delete

11.
Write a script that counts the number of directories and sub-directories in the current directory.

The current and parent directories should not be taken into account
Hidden directories should be counted
find . -type d -mindepth 1 | wc -l

12.
Create a script that displays the 10 newest files in the current directory.

Requirements:

One file per line
Sorted from the newest to the oldest
ls -t | head -n10

13.
Create a scripts that takes a list of words as input and prints only words that appear exactly once.

Input format: One line, one word
Output format: One line, one word
Words should be sorted
sort | uniq -u

14.
Display lines containing the pattern "root" from the file /etc/passwd
grep root /etc/passwd

15.
Display the number of lines that contain the pattern "bin" in the file /etc/passwd
grep -c bin /etc/passwd

16.
Display lines containing the pattern "root" and 3 lines after them in the file /etc/passwd.
grep -A3 "root" /etc/passwd

17.
Display all the lines in the file /etc/passwd that do not contain the pattern "bin".
grep -v "bin" /etc/passwd

18.
Display all lines of the file /etc/ssh/sshd_config starting with a letter.

include capital letters as well
grep ^[a-zA-Z] /etc/ssh/sshd_config

19.
Replace all characters A and c from input to Z and e respectively.
tr [Ac] [Ze]

20.
Create a script that removes all letters c and C from input.
tr -d cC

21.
Write a script that reverse its input.
rev

22.
Write a script that displays all users and their home directories, sorted by users.
cat /etc/passwd | cut -f1,6 -d ':' | sort

https://intranet.hbtn.io/projects/208