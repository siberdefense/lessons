# [Transformation](https://play.picoctf.org/practice/challenge/104)

## Prompt
I wonder what this really is... [enc](./enc)

```''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0,
len(flag), 2)])```

## Guide


## Skills & Concepts
- Reading Python source code