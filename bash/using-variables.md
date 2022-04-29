### Declaring variables in your bash script

There are a few caveats while declaring variables in bash. Assigning of vairables should be done without any spaces before or after the `=` sign. We don't have the liberty of having spaces in between the variable name, the equal to operator and the assigned value like in other programming languages. For a beginner who hasn't grasped how bash understands these spaces it can be annoying trying to fix these bugs

If you say

```bash
command= pwd
```

the variable `command` is set to the empty string, for the duration of executing the `pwd` command.

```bash
command= 
```

This sets the `command` variable to an empty string

```bash
command = pwd
```

This will try to run `command` with arguments `=` and `pwd`