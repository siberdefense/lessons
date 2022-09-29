# [Information](https://play.picoctf.org/practice/challenge/186)

## Prompt

Files can always be changed in a secret way. Can you find the flag?
[cat.jpg](cat.jpg)

## Guide

A JPEG file is provided with a hint to view its "details."

Open the image in a viewer and search the menus for a way to display image
details. The specifics will depend on which program is used to view the file.
Alternatively, install `exiftool` and dump the image metadata.

The license metadata field contains a suspiciously garbled value.

We take a guess that it's encoded somehow. The first thing to try is Base 64.
Helpfully, a program called `base64` is availble from our Linux terminal. Use
its `man` page to find a flag that looks useful for decoding. The `man` page
also tells you how the `base64` programs expects data.

## Skills & Concepts
- Data encoding/decoding concepts.
- Use `apt` to install software on Ubuntu.
- Use `man` pages to learn how to use a program.
- Use `echo` to repeat a string.
- Use the `|` pipe operator to chain commands together.

## [Solution](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnQwYUdWZmJUTjBZV1JoZEdGZk1YTmZiVzlrYVdacFpXUjk)