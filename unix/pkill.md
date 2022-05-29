## pkill command in unix

The `pkill` command is a handy tool to kill off multiple processes at once, rather than grepping all their process ids and then killing them manually.


```bash
pkill chrome
```

The above command will kill all the processes which has `chrome` in its name. You can also pass signals to either kill the processes, or reload them. By default they'll be stopped gracefully.

Examples:

```bash
pkill -KILL airbyte*
``` 

```bash
pkill -9 airbyte* 
```

