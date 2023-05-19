# Command find
# -empty
* One interesting command-line option to use with `find` is `-empty`.
* This command searches for empty files and directories.
* I added an empty file within the file 911report, so when I use the `find` and `-empty` command on `./911report` (`.` being `/Users/giannaalcasid/Downloads/stringsearch-data-main/technical`), the terminal prints out the path of the empty file.
* When I use the same commands on `./biomed`, which doesn't have any empty files, the terminal doesn't print out anything.
* These are useful when searching for empty files and directories, and a user can make sure they have no empty files. If they do, detecting the existence and location of the empty file allows the user to delete it.
* Sources: [https://www.geeksforgeeks.org/find-command-in-linux-with-examples/](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/) & manual for `find` by typing in `man find` into terminal  
```
giannaalcasid@Giannas-MacBook-Air technical % find ./biomed -empty
```
```
giannaalcasid@Giannas-MacBook-Air technical % find ./911report -empty
./911report/emptyFile
```

# -name
* Another command-line option is `-name`.
* This command searches for files with the name specified.
* Here, I changed the directory to be `/Users/giannaalcasid/Downloads/stringsearch-data-main` by doing `cd ..`.
* After this, I used the `find` command to find files with the name chapter-1.txt and rr196.txt within the `.technical` directory.
* When running these commands, it displays the file path the file is located in and the name of the file.
* These are useful because it can be difficult to scan through many files to look for a file with a specific name, as it's easy to pass by the one you're looking for, or mistake a similarly named file as the one you're looking for.
* Sources: [https://www.geeksforgeeks.org/find-command-in-linux-with-examples/](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/) & manual for `find` by typing in `man find` into terminal
```
giannaalcasid@Giannas-MacBook-Air stringsearch-data-main % pwd
/Users/giannaalcasid/Downloads/stringsearch-data-main
giannaalcasid@Giannas-MacBook-Air stringsearch-data-main % find .
/technical -name chapter-1.txt
./technical/911report/chapter-1.txt
```
```
giannaalcasid@Giannas-MacBook-Air stringsearch-data-main % find ./technical -name rr196.txt    
./technical/biomed/rr196.txt
```

# -user
* This command-line option is `-user`, and it searches for files owned by the specified username in the directory stated.
* In these two examples, I search for files owned by user giannaalcasid in emptyFile and Alcohol_Problems, found in 911report and government respectively.
* In emptyFile, there is nothing inside, but I own this file so it outputs the directory of emptyFile.
* However, in the Alcohol_Problems file, there are 4 files owned by me, and the terminal outputs the name of each file owned by the user found in that directory.
* These are useful because when working with other files, some parts of it may be owned by another user. There may be similar files, but a user might want to only search for the one that they own, or make sure all of the files they own are in their own file and not in anybody else's.
* Sources: [https://www.geeksforgeeks.org/find-command-in-linux-with-examples/](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/) & manual for `find` by typing in `man find` into terminal
```
giannaalcasid@Giannas-MacBook-Air stringsearch-data-main % find ./technical/911report/emptyFile -user giannaalcasid
./technical/911report/emptyFile
```
```
giannaalcasid@Giannas-MacBook-Air stringsearch-data-main % find ./technical/911report/emptyFile -user giannaalcasid
./technical/911report/emptyFile
giannaalcasid@Giannas-MacBook-Air stringsearch-data-main % find ./technical/government/Alcohol_Problems -user giannaalcasid
./technical/government/Alcohol_Problems
./technical/government/Alcohol_Problems/Session2-PDF.txt
./technical/government/Alcohol_Problems/Session3-PDF.txt
./technical/government/Alcohol_Problems/DraftRecom-PDF.txt
./technical/government/Alcohol_Problems/Session4-PDF.txt
```

# -type
* The command-line option `-type` is true if the file is of the specified type.
* There are many types to test, but for these examples, I will use directory (d) and regular file (f).
* In the first example, I am searching within `./technical` and I want the terminal to print all the directories. It traverses through the directory and prints by order, and this is useful when wanting to see all possible directories without including possible files in them.
* In the second example, I am searching within the 911report folder and looking for all the files in it. This is useful because a folder might contain other folders, but you only want to know the files contained within.
* Sources: [https://www.geeksforgeeks.org/find-command-in-linux-with-examples/](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/) & manual for `find` by typing in `man find` into terminal 
```
giannaalcasid@Giannas-MacBook-Air stringsearch-data-main % find ./technical -type d
./technical
./technical/government
./technical/government/About_LSC
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Gen_Account_Office
./technical/government/Post_Rate_Comm
./technical/government/Media
./technical/plos
./technical/biomed
./technical/911report
./technical/911report/emptyFile
```
```
giannaalcasid@Giannas-MacBook-Air stringsearch-data-main % find ./technical/911report -type f
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
```
