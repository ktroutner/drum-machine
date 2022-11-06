# About the beat files

The format of a beat file should be as follows:

```
1 1 1 2 2 2 1 1 1
120

pitch_numXX XX XX
pitch_num X  X  X
pitch_numXXXXXXXX

pitch_numX   X   
pitch_num X X X X
```

The first line tells the sequence of patterns to be played, where i refers
to the ith pattern listed below.  There should be a space separating each
pattern number.

The second line is the initial tempo.

Patterns are separated by blank lines (these lines cannot have whitespace!).
Note also that there is a blank line between the sequence line and the first
pattern.

Patterns consist of multiple consecutive lines in the format above.
`pitch_num` is a 2-digit number representing the drum piece to be played.
The pitch number is followed by a sequence of `X`'s and spaces, where an `X`
means that this note should be played at the corresponding eighth-note time
step, and a space represents that this note should not be played (it will be
turned off).

**IMPORTANT**
Note that there is no space between the pitch number and the beginning of the
sequence.  A space immediately following the pitch number indicates that
the given note will not be played at the first time step.

For some examples of proper format, see `beat1.txt` and `beat2.txt`.

# References
- Created for a [course project](https://www.cs.cmu.edu/~music/cmsip/projects/p3.pdf)
- Implemented using [serpent](https://www.cs.cmu.edu/~music/serpent/doc/serpent.htm)
