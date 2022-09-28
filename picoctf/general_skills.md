# PicoCTF Gym Challenge Notes

## General Skills

### Obedient Cat

A link to a file is provided. The file contain the clear-text flag.

Skills & concepts
- Files and directories
- Linux command line basics
- Using `wget` or `curl` to download files at the command line
- Using `nano` to view and edit text files from the command line

### Mod 26

Some cipher-text is provided with a hint to use ROT-13.

Skills & Concepts
- Caesar ciphers
- Using [CyberChef](https://gchq.github.io/CyberChef/)

### Python Wrangling

Download and run a Python script.

### Wave a Flag

Download a program invoke it with a --help flag. Also try -h and -help.

Use `chmod` to make the program file executable.

### Information

A JPEG file is provided with a hint to view its "details."

Open the image in a viewer and search the menus for a way to display image
details. The specifics will depend on which program is used to view the file.
Alternatively, install `exiftool` and dump the image metadata.

The license metadata field contains a suspiciously garbled value.

We take a guess that it's encoded somehow. The first thing to try is Base 64.
Helpfully, a program called `base64` is availble from our Linux terminal. Use
its `man` page to find a flag that looks useful for decoding. The `man` page
also tells you how the `base64` programs expects data.

Skills & Concepts
- Data encoding/decoding concepts.
- Use `apt` to install software on Ubuntu.
- Use `man` pages to learn how to use a program.
- Use `echo` to repeat a string.
- Use the `|` pipe operator to chain commands together.

### Nice Netcat

Skills & Concepts
- Networking: IP addresses, hostnames, DNS & ports
-