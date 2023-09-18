# Somewhat advanced Container/Linux/Bash/Terminal Notes

Very similar to docker, you download images and you can create containers from images. Containers are like there own computers that are completely seperate from your computer, and they can allow you to run true linux distros, such as ubuntu, arch, busybox, alpine, etc.

## Podman Commands

* `podman start -a <name>` attach to a container

* `podman --help` - get help for all podman commands
* `podman images` - see the current images you have downloaded
* `podman ps -a` - to show all countainers (running and exited)
* `podman ps` - just show running containers
* `podman pull ubuntu` - pull down a new image from the internet, in this case it will pull down the latest ubuntu image from the default registry (which is docker hub).
* `podman pull docker.io/library/ubuntu:latest` - does the same thing as the last command, but is the full version
* `podman run -it` - (i stands for interactive, t stands for terminal) (add --rm to throw the container away when you exit)
* `podman rm <name>` - to remove containers
* `podman run -it --hostname boost --name boost ubuntu` - run a new ubuntu container, first by checking downloaded images for an image called ubuntu, and then looking through the default registry for images named ubuntu to download and use. it will have the hostname of boost and the name of boost, instad of random names.

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
