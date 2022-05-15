# Line endings

Windows uses carriage return + line feed as its line ending character, while unix systems uses just a single line feed. If you dockerfile was written in a Windows machine and you're trying to run it on Mac/Linux or vice versa, you will encounter the following error, if you haven't handled the line endings properly.

```bash
standard_init_linux.go:228: exec user process caused: no such file or directory
```