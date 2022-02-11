# Lab Report 3

## Streamlining `ssh` Configuration

`config` file:
![Image](report-3\1.png)
To make the config file, it was easiest to make a file in the folder and edit it with notepad, then remove the file extention. `ieng6` is the alias used for `cs15lwi22aid@ucsd.edu`. I also added the `IdentityFile` line because `scp` wasn't working without it. (`ssh` worked regardless)

`ssh`ing with alias
![Image](report-3\2.jpg)
`ssh` works with the alias. I connected to the remote server by using it's hostname. Typing `ssh ieng6` instead of `ssh cs15lwi22aid@ieng6.ucsd.edu` makes the process much faster.

`scp`ing with alias
![Image](report-3\3.png)
`scp` works with the alias. I copied my `MarkdownParse.java` to the `markdown-parse/` folder on the server.