## scp to securely copy files over SSH

You can use the `scp` command to copy files from your local machine to a remote machine which you have access to via SSH.

```bash
scp -i ./path/to/key.pem /path/to/file.md username@host:/path/to/copy/in/remote
```

Or if you already have added your public key in the `authorized_keys`

```bash
scp /path/to/file.md username@host:/path/to/copy/in/remote
```


