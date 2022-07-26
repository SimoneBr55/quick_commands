```
find /directory_path -mtime -1 -ls
```


```
find . -mtime 0 -printf '%T+\t%s\t%p\n' 2>/dev/null | sort -r | more
```

```
find /var -name "*.php" -mtime -1 -ls
```
