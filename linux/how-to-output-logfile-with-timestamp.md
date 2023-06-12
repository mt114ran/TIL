# How to output log file with timestamp

>
To output the output of a Linux command with a timestamp in a log file

---
### most used usage
If you want to display the result of the "ls" command in the current directory, with the filename "result_yyyymmddhhmm.log" (where "yyyymmddhhmm" represents the timestamp), you can execute the following command:
```sh
ls 2>&1 | tee -a ./result_$(date +%Y%m%d%H%M).log
```
---
### Manual


* **2>&1** : It means put standard error output (2) into standard output (1).
* **|** : Used to bridge the standard output of a Linux command to the next command.
* **tee** : Branch standard output to display (standard output) and output to file.
* **-a** : options of tee command. Append to the output file if it exists, create a new one if it does not exist.
* **$(date +%Y%m%d%H%M)** : add timestamp.

You may not need the a option of the tee command if you want to add a timestamp. . .

<br>

*2023.6.12*
