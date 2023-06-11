# Use grep commands

> Here are some examples of using the grep command:

---
### most used usage
* -r : search inside directories
* -i : Search case-insensitively
* -n : Show line numbers in search results
```sh
grep -rin Test .
```

---
### Example of use

If you want to search for the letter "a" within all files in the "work" directory
```sh
grep a work/*
```
<br>

With grep, you can set two or more conditions and display lines that meet both conditions, and (and) search.
```sh
grep a work/* | grep b
```
<br>

-i option : Search case-insensitively
```sh
grep -i test work/*
```
<br>

-n option : Show line numbers in search results
```sh
grep -n test work/*
```
<br>

-o option : Display matching characters in search results
```sh
grep -o test work/*
```
<br>

-C options : Display the specified number of n lines before and after the location where the search results match
```sh
grep -C n test work/*
```
<br>

-r oprions : Also search inside directories
```sh
grep -r test work/*
```
<br>

*2023.6.11*
