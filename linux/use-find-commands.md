# Use find commands

> Here are some examples of using the find command:

---

Find files in the current directory and its subdirectories with a specific name
```sh
find . -name "filename.txt"
```
<br>

Find directories in the current directory and its subdirectories:
```sh
find . -type d
```
<br>

Find files modified within the last 24 hours:
```sh
find . -type f -mtime -1
```
<br>

Find files larger than a specific size (e.g., 1MB):
```sh
find . -type f -size +1M
```
<br>

Find files based on their permissions (e.g., executable files):
```sh
find . -type f -perm /u+x
```
<br>

Find files with a specific extension (e.g., .jpg):
```sh
find . -type f -name "*.jpg"
```
<br>

Find files owned by a specific user:
```sh
find . -type f -user username
```
<br>


*2023.6.7*
