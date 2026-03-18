# Rob Pike's 5 Rules of Programming

Use these as default rules when writing or reviewing code in this repository.

## The 5 rules

1. You can't tell where a program is going to spend its time. Bottlenecks occur in surprising places, so do not add speed hacks until a bottleneck is proven.
2. Measure. Do not tune for speed until you have measured, and even then only optimize when one part dominates.
3. Fancy algorithms are often slower for small `n`, and `n` is usually small. Avoid complexity until data proves otherwise.
4. Fancy algorithms are buggier and harder to implement than simple ones. Prefer simple algorithms and simple data structures.
5. Data dominates. Choose and organize data structures well; the right algorithms usually become obvious.

## Practical application in this repo

- Prefer straightforward implementations first, then optimize with evidence.
- Require profiling/measurement notes before performance-oriented refactors.
- Favor readable code and simple structures over cleverness.
- Evaluate data model choices before introducing algorithmic complexity.

## Source

- Rob Pike's 5 Rules of Programming: https://www.cs.unc.edu/~stotts/COMP590-059-f24/robsrules.html
