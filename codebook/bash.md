## General Commands (already basic knowledge)

* `sudo su -` become the **root** user, this will require a password.
* `cat` - displays a file in the terminal
* `echo <text> >> <file>` - adds the text to a file
* `more FILE` - pager that allows you to page through files (without having to scroll). You can also search the file by typing `/` and then the term you want to search by. Has arrow key suport.
* `head FILE` / `tai FILE` - read the beginning and end of a file respectively
* `head -1 FILE` - read the first line of a file
* `> FILE` - "zero outs" (erases) the file's contents
* 

### Piping

* `ls -al | more` - takes the standard output of `ls -al` and sends it into the `more` command.
* `ls -al > FILE` - takes the standard output of `ls -al` and writes it to a file.
* `echo TEXT >> FILE` - appends the text to the end of the file.
