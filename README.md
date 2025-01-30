# Make Make Make Make Make Make Make 🤖

Collections of Makefile experiments

## Learnings

- Makefile system determines whether a file changed based solely upon timestamp
    - If A depends on B, and A is older than B, guess what - A's gettin' made, babe.
- First rule is the one run by default; by convention, this should be the `all` command
- Similarly, Makefiles typically include a `clean` command
- Each rule follows the pattern `<TARGET_FILE>: <DEPENDENCY>`
- Obviously, if a target file does not exist, then the commands for that rule get executed
    - This is why `all` typically does not output to any file
- Makefiles require tabs, not spaces

## Resources

- Learn make in 60 seconds - https://www.youtube.com/watch?v=a8mPKBxQ9No
- Makefiles Make Your Life Easier - https://www.youtube.com/watch?v=yWLkyN_Satk
- Makefiles: 95% of what you need to know - https://www.youtube.com/watch?v=DtGrdB8wQ_8
