# dt command in vim to delete upto a particular character

In vim you use `dd` to delete an entire line of text.

You can use the `dt` to delete text upto a particular character. For example, the following command will delete all the text from wherever the cursor is to the next instance of `"`

```vimscript
dt"
```

This makes it really easy to delete a particular section of text without having to select it.