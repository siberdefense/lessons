# [Wireshark doo dooo do doo...](https://play.picoctf.org/practice/challenge/115)

## Prompt

Can you find the flag? [shark1.pcapng](shark1.pcapng).

## Guide

1. Open the provided file in Wireshark.
2. Get overwhelmed by the volume of data to review.
3. Try (and fail) to skim every packet for something that jumps out as interesting.
4. Look for ways to reduce the amount of data.
5. Use the Wireshark view filter to view a single stream (collections of related packets from
   the same session) and
   then use Analyze->Follow->TCP Stream to see a condensed view of the stream.
6. Notice the following in the 5th stream (view filter `tcp.stream eq 5`):

```
Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}
```

That sure looks like the structure of a flag, so we solved the first
portion of the challenge. Now on to part 2, data decoding.

7. We know PicoCTF flags have the following structure:
   `picoCTF{leet_speak_goop}`.
8. Might this be a simple Caesar alphabet rotation cipher?

## Skills & Concepts
- Network packet capture analysis
- Data decoding & manipulation

## Solution
```sh
# Set up temporary Python environment
$> virtualenv --python python3 --prompt="pico" tempvenv
$> source tempvenv/bin/activate

# Install a Caesar cipher helper
$> pip install caesarcipher

# Decrypt the message
$> caesarcipher -d -o 13 "Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}"

# Clean up
$> tempvenv/bin/deactivate
$> rm -rf tempvenv
```