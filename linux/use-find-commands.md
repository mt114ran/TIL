# Use find commands

> Here are some examples of using the find command:

---

Find files in the current directory and its subdirectories with a specific name
```bash
find . -name "filename.txt"
```
<br>

Find directories in the current directory and its subdirectories:
```bash
find . -type d
```
<br>

Find files modified within the last 24 hours:
```bash
find . -type f -mtime -1
```
<br>

Find files larger than a specific size (e.g., 1MB):
```bash
find . -type f -size +1M
```
<br>

Find files based on their permissions (e.g., executable files):
```bash
find . -type f -perm /u+x
```
<br>

Find files with a specific extension (e.g., .jpg):
```bash
find . -type f -name "*.jpg"
```
<br>

Find files owned by a specific user:
```bash
find . -type f -user username
```
<br>


*2023.6.7*
