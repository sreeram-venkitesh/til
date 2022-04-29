Using `basename` we can extract the filename of a file that we downloaded using `wget` or `curl`

```bash
url=http://example.com/test.zip
wget $url 
filename=$(basename "$url")
unzip $(basename "$url")
```

In the above example this is used when we need to get the filename from the url so that we can unzip the actual file. Here this can be done since the filename is present in the url.