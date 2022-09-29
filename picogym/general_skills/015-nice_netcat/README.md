# [Nice Netcat](https://play.picoctf.org/practice/challenge/156)

## Prompt

There is a nice program that you can talk to by using this command in a shell:
```sh
nc mercury.picoctf.net 49039
```
but it doesn't speak English...

## Guide

Try reading a little about the netcat command using `man netcat`. Then run the
command about to connect to the challenge server.

The server responds with numbers.

Let's save the server's response to a file so its easier a little easier to work
with.

```sh
nc mercury.picoctf.net 49039 > server_output.txt
```

## Skills & Concepts
- Networking: IP addresses, hostnames, DNS & ports
- Data encoding/decoding. Specifically ASCII encoding.
- Linux command line skills: redirecting program output to a file

## [Solution](https://gchq.github.io/CyberChef/#recipe=From_Decimal('Line%20feed',false)&input=MTEyIAoxMDUgCjk5IAoxMTEgCjY3IAo4NCAKNzAgCjEyMyAKMTAzIAo0OCAKNDggCjEwMCAKOTUgCjEwNyAKNDkgCjExNiAKMTE2IAoxMjEgCjMzIAo5NSAKMTEwIAo0OSAKOTkgCjUxIAo5NSAKMTA3IAo0OSAKMTE2IAoxMTYgCjEyMSAKMzMgCjk1IAo1MSAKMTAwIAo1NiAKNTIgCjEwMSAKMTAwIAo5OSAKNTYgCjEyNSAKMTAgCg)