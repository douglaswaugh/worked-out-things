Work out how to output file of unique lines matching pattern in files with names matching pattern
===

1. Find all files matching pattern, and grep the files for lines matching pattern
```
find -name [file-name-pattern] -exec grep -i '[line-pattern]' {} > [output-file-name] \;
```

2. Sort the lines in the file and write unique ones back to the file. N.B. [input-file-name] and [output-file-name] can be the same file.
```
sort [input-file-name] | uniq -u > [output-file-name]
```