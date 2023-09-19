## General Commands (already basic knowledge)

* `sudo su -` become the **root** user, this will require a password.
* `cat` - displays a file in the terminal
* `echo <text> >> <file>` - adds the text to a file
* `more FILE` - pager that allows you to page through files (without having to scroll). You can also search the file by typing `/` and then the term you want to search by. Has arrow key suport.
* `head FILE` / `tai FILE` - read the beginning and end of a file respectively
* `head -1 FILE` - read the first line of a file
* `> FILE` - "zero outs" (erases) the file's contents 

### Piping

* `ls -al | more` - takes the standard output of `ls -al` and sends it into the `more` command.
* `ls -al > FILE` - takes the standard output of `ls -al` and writes it to a file.
* `echo TEXT >> FILE` - appends the text to the end of the file.

### Find

* `find / -name '*zet*'` - searches the entire system to find all the files with "zet" somwhere in their title. Note that the `*` mean that anything can be on either side of the world zet for the find command to output that file.
* `find DIR -name '<name>'` - searchs everything within DIR (including other directories) for something named the name provided. The `/` directory searches the entire system, and this will give you errors because you do not have permission to search some files.
* `find / -name '*zet*' 2>/dev/null` - since search the entire system returns unwanted and unnecessary errors, you can add `2>/dev/null` to send these errors to the trash where they will be deleted so you do not need to see them.
* `find / -name '*zet*' 2>/dev/null | less` - if you have a lot of results, you can pipe the standard output to the pager `less` in order to read through them.
* `find / -name '*zet*' 2>/dev/null 1>/tmp/foo` - redirect and save the standard output (stdout) in a file at `/tmp/foo`
