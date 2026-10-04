# Plurality

A command-line plurality election written in C for CS50. The candidate with the most votes wins, and if several candidates tie for the most votes, all of them are printed.

## How it works

The program starts with the CS50 distribution code (the `candidate` struct, the `candidates` array, and `main`). I implemented two functions:

- `vote(string name)` looks through the candidates for a matching name. If it finds one, it adds a vote and returns `true`. If nobody matches, it changes nothing and returns `false`, and `main` prints "Invalid vote."
- `print_winner(void)` makes two passes over the candidates. The first pass finds the highest vote total. The second pass prints every candidate with that total, so ties are handled correctly. The candidates are never sorted.

## Compile and run

```
make plurality
./plurality Alice Bob Charlie
```

Enter the number of voters, then type one vote per line. Names must match the command-line names exactly, including capitalization.

```
Number of voters: 4
Vote: Alice
Vote: Charlie
Vote: Bob
Vote: Alice
Alice
```

## Testing

- Passes all `check50` checks for `cs50/problems/2026/x/plurality`
- Tested manually with an ordinary election, a tie, and an invalid vote

## Notes

Part of CS50's Problem Set 3. Spec: https://cs50.harvard.edu/x/psets/3/plurality/
