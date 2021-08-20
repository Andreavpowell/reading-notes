# Errors and Debugging

## The Stack
- JavaScript interpreter processes one line of code at a time. When a statement needs data from another function, it stacks (piles) the new function on top of the current task
- Understanding execution contexts and stacks, its easier to find errors
- debugging involves a process of deduction
- console helps narrow down the area in which the error is located, so you can try to find the exact error
- JS has 7 different types of errors where each creates its own error object and can tell you its line number and a description
- if you know you're going to get an error, you can handle it using the `try`, `catch`, `finally` statements. 

[Home](reading-notes)

test