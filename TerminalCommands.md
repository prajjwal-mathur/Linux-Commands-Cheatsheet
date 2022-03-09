## Commands known:
- To see what's in the file(first to last): [`cat <location/filename>`](https://www.geeksforgeeks.org/cat-command-in-linux-with-examples/)
- To look at a file backwards, starting with the last line: `tac <location/filename>`
- To show the first 10 lines(default) of a file: [`head <location/filename>`](https://linuxize.com/post/linux-head-command/#head-command-syntax)
- To show the first 'n' lines of a file: `head -n <location/filename>`
- To show the last 10 lines(default) of a file: [`tail <location/filename>`](https://linuxize.com/post/linux-head-command/#head-command-syntax)
- To show the last 'n' lines of a file: `tail -n <location/filename>`
- To view documentation: [`man <program name or command like python>`](https://www.geeksforgeeks.org/man-command-in-linux-with-examples/)
- To gain root/administrative access(prompts for password): `sudo`  
- To stop the graphical interface: `sudo systemctl stop gdm (or sudo telinit 3)`
- To start the graphical interface: `sudo systemctl start gdm (or sudo telinit 5)`
- To halt the system(requires superuser access): `shutdown -h`
- To reboot the system(requires superuser access): `shutdown -r`
- When administering a multi-user system, we have the option of notifying all users prior to shutdown:
`sudo shutdown -h <time> "Message"`
- To find the address of an installed program: `which <app>` or `whereis <app>`
- To display the print working directory: `pwd`
- To change the directory to home directory from the current working directory(current working directory replaces terminal's home directory in history): `cd` or `cd ~`
- To go to parent directory of the current working directory: `cd ..`
- To go back to previous directory: `cd -`
- To list all the contents of working directory: `ls`
- To list all the contents including hidden files of working directory: `ls -a`
- To get the tree view of the filesystem(`sudo apt install tree` for first time): `tree`
- To get the tree view of only directories not files: `tree -d`
- `cd` command remembers the moving history, to see the history: `dirs`
- To push a directory in history for easy use: `pushd </foldername>`
- To delete the directory added recently from history: `popd` 
- To create an empty file: `touch <filename>`
- To display and redirect ouput of a command: [`tee`](https://linuxize.com/post/linux-tee-command/)
- To create a new file from the terminal: `touch filename.extension`
- To create a new file with specific date(time: 24-hour format; LowerLimit of year: 1901):
    - In string format: `touch -d "YYYY-MM-DD hh:mm:ss" filename.extension`
    - In Integer-ish format: `touch -t YYYYMMDDhhmm.ss filename.extension`
    
>    *For example:<br/>
touch -d "2010-01-02 00:01:00" xyz.txt<br/>
touch -t 201001020001.00 xyz.txt<br/>
Both the above commands create a text file "xyz.txt" with creation date as 02-January-2010 at 12:01 a.m.*

- To create a directory/folder: `mkdir folderName` or `mkdir location/foldername`
- To remove an empty directory: `rmdir folderName`
- To remove a directory along with its contents: `rm -rf folderName`
- To rename a file/directory: `mv FileName newFileName`
- To remove a file: `rm fileName`
- To forcefully remove a file: `rm –f`
- To interactively remove a file(it asks if you're sure to delete or not): `rm -i`
- To locate a file: `locate filename`

- To list all files in the current directory and all of its subdirectories: `find`
- To search for files and directories in a folder: `find /folder -name filename`
- To search only for directories: `find /folderName -type d -name somethingToBeFound`
- To search only for regular files: `find /folderName -type f -name somethingToBeFound`
    - Commonly used options to shorten the list include:
        - -name (only list files with a certain pattern in their name)
        - -iname (also ignore the case of file names)
        - -type (which will restrict the results to files of a certain specified type, such as d for directory, l for symbolic link, or f for a regular file, etc.)
- To kill a process(you can only kill your own processes; those belonging to another user are off limits, unless you are root): `kill -SIGKILL <pid>` or `kill -9 <pid>.` 
- To see the processes running: `ps -aux` or `htop`
- To get task manager-ish view of processes running: `top`
- To see the processes in tree-view: `pstree`
- To display all jobs running in background(shows the job ID, state, and command name): `jobs`
- To display all jobs running in background(adds the PID of the background jobs to normal jobs commands): `jobs -l`
- To display information about mounted filesystems, including the filesystem type, and usage statistics about currently used and available space: `df -Th`
- To compare two text files(for binary: replace with `cmp`): `diff [options] <file1> <file2>`
    > Options
    - `-c` : Provides a list of differences with 3 lines of context
    - `-r` : Used to recursively compare subdirectories along with present directory
    - `-i` : To ignore the case of letters
    - `-w` : To ignore white spaces and tabs
    - `-q` : To return only if files are different without listing differences 
- To compare three text files with one as reference: `diff3 <file1> <common-reference-file> <file3>`
- To get the extension of a file: `file <fileName>`
- To sync files between hosts: [`rsync`](https://www.geeksforgeeks.org/rsync-command-in-linux-with-examples/)
- Two Ways to add lines to text:
    - To add a line to a text file: `echo message>filename`
    - To append the line to text file: `echo message2>>filename`
        - Example(both ways do the same thing):
            - echo message 1 > myfile<br/>echo message 2 >> myfile<br/>echo message 3 >> myfile
            - cat << EOF > myfile<br/>> message 1</br>> message 2<br/>> message 3<br/>> EOF
            > Above both codes do the same:<br/>
            message 1<br/>message 2<br/>message 3 
- To get tutorial about vim (Vi IMproved): `vimtutor`
    - Commands in vim editor:
        - Start the editor and edit file: `vi filename`
        - Start and edit file in recovery mode(recover file after a crash): `vi -r filename`
        - Read in file and insert at current position: `:r fileName`
        - Write to the file: `:w`
        - Write out to file: `:w file`
        - To overwrite file: `:w! file`
        - To exit and write out modified file: `:x` or `:wq`
        - To quit: `:q`	
        - To quit without saving: `:q!`	
        - To count the words in a file in vim editor: `:! wc %`
- To identify current user: `whoami`
- To identify all logged-on user: `who`
- To retrieve currently defined aliases: `alias`
- To define a new user: `sudo useradd <username>`
- To delete a user: `sudo userdel <username>`
- To temporary become a super-user: `su`
- To view the files present in the current directory in the long listing format: `ls -l`
- When working with compressed files, most associated utilities required to work have 'z' prefixed to their name:
    - To view a compressed file: `zcat compress_file`
    - To page through a compressed file(it's a filter): `zless compressed-file` or `zmore compressed-file`
    - To search inside a compressed file(-i ignores the case): `zgrep -i "whatever-you-want-to-search" compressed-file`
    - To compare two compressed files: zdiff file1 file2
- To sort the lines, according to the characters at the beginning of each line: `sort <filename>`
- To combine the two files and sort the lines, then display the output to the terminal: `cat file1 file2 | sort`
- To sort the lines in reverse order: `sort -r <filename>`
- To sort the lines by the 3rd field on each line instead of the beginning: `sort -k 3 <filename>`
- To sort the list with removed duplicates, only uniques: `sort -u <filename>`
- To remove duplicate entries from multiple files at once: `sort file1 file2 | uniq > file3` or sort -u file1 file2 > file3
- To count the number of duplicate entries: `uniq -c filename`
- To paste contents from two files in a table format(first line of first file will correspond to first line of second file in a row): `paste file1 file2`
- To paste contents from two files with a delimiter like dash(-)or colon(:)(For example: xyz-123, in this xyz is from first and 123 is from second): `paste -d "delimiter" file1 file2`
- If two files have a common column and you want to merge them in a single file: `join file1 file2`
- To split a text file into equal files of n lines(the 100 newfile names will be suffixed with xx which aa..ab..ac): `split -n "number of files to be splitted in" <file_that_needs_to_be_split> <newfile>`
- Regex(REGular EXpression; used for searching a particular pattern):
    - Match any single character: `.`
    - Match a or z: `a|z`
    - Match end of a line: `$`
    - Match beginning of a line: `^`
    - Match a preceding item 0 or more times: `*`
- To search for a pattern in a file and print all matching lines: `grep [pattern] <filename>`
- To print lines that exclude a certain pattern: `grep -v [pattern] <filename>`
- TO print the lines that contain the numbers 0 through 9: `grep [0-9] <filename>`
- To print context of lines (specified number of lines above and below the pattern) for matching the pattern. Here, the number of lines is specified as n: `grep -C n [pattern] <filename>`
- To convert lower case to upper case(tr stands for translate): `cat filename | tr a-z A-Z`
- To display the number of lines: `wc -l filename` 
- To display the number of bytes: `wc -c filename`
- To display the number of words: `wc -w filename`
- To check the status of the remote host: `ping <hostname>`
- To show current routing table: `route –n` or `ip route`
- To add a static route: `route add -net address` or `ip route add`
- To delete a static route: `route del -net address` or `ip route del`
- To download a web-page: `wget <url>`
- To read a web-page from terminal: `curl <url>`
- To get the contents of a web page and store it to a file: `curl -o filename_to_be_saved url`
- To copy a local file to a remote system in the command prompt: `scp <localfile> <user@remotesystem>:/home/user/`
- To make a shell script for easy automation, you need a .sh file
- Functions in a script file: `function(){ echo "This is a sample function"}`
- Syntax for if-else:<br /> 
    if [condition file]; <br />
    then<br />
    &emsp; statements<br />
    else<br />
    &emsp;    statements<br />
    fi<br />
- Conditions for if:
    - Checks if the file exists: `-e`
    - Checks if the file is a directory: `-d`
    - Checks if the file is a regular file (i.e. not a symbolic link, device node, directory, etc.) : `-f`
    - Checks if the file is of non-zero size: `-s`
    - Checks if the file has [sgid](https://www.geeksforgeeks.org/finding-files-with-suid-and-sgid-permissions-in-linux/) set: `-g`
    - Checks if the file has suid set: `-u`
    - Checks if the file is readable: `-r`
    - Checks if the file is writable: `-w`
    - Checks if the file is executable: `-x`
- Logical operators to be used with if[expression1 -operation expression2]:
    - Equal to: `-eq`
    - Not equal: `-ne
	- Greater than: `-gt`
	- Less than: `-lt`
	- Greater than or equal to: `-ge`
	- Less than or equal to: `-le`
    - Compares the sorting order of string1 and string2: `[[ string1 > string2 ]]`
    - Compares the characters in string1 with the characters in string2: `[[ string1 == string2 ]]`
    - Saves the length of string1 in the variable myLen1: `myLen1=${#string1}`
- Switch statement:<br />
case expression in<br />
   &emsp;pattern1)&emsp;execute commands ;;<br />
   &emsp;pattern2)&emsp;execute commands ;;<br />
   &emsp;pattern3)&emsp;execute commands ;;<br />
   &emsp;pattern4)&emsp;execute commands ;;<br />
   &emsp;*&ensp;)&emsp;execute some default commands or nothing ;;<br />
esac
- Three types of loops are often used in most programming languages:
    - `for` loop:<br />
        for variable-name in list<br />
        do<br />
        &emsp;execute one iteration for each item in the list until the list is finished<br />
        done
    - `while` loop:<br />
        while condition is true<br />
        do<br />
        &emsp;Commands for execution<br />
        done
    - `until` loop; it repeats a set of statements as long as the control command is false:<br />
        until condition is false<br />
        do<br />
        &emsp;Commands for execution<br />
        done
- To edit/debug a script(to exit: write `+ exit 0` at the end of file): `script.sh debug`
- To create a temporary file: `TEMP=$(mktemp /tmp/tempfile.XXXXXXXX)`
- To create a temporary directory: `TEMPDIR=$(mktemp -d /tmp/tempdir.XXXXXXXX)`
- To generate a random number: `$RANDOM`
- To get the length of a string: `${#string}` or `expr length $string`
- Printing Operations:
    - To print the file to default printer: `lp <filename>`
    - To print to a specific printer (useful if multiple printers are available): `lp -d printer_id <filename>`
    - To print the output of a program: `program | lp
echo string | lp`
    - To print multiple copies: `lp -n number <filename>`
    - To set the default printer: `lpoptions -d printer`
    - To show the queue status: `lpq -a`
    - To configure printer queues: `lpadmin`
    - To get a list of available printers, along with their status: `lpstat -p -d`
    - To check the status of all connected printers, including job numbers: `lpstat -a`
    - To cancel a print job: `cancel job-id` OR `lprm job-id`
    - To move a print job to new printer: `lpmove job-id newprinter`
-  To convert a text file to two columns (-2) formatted PostScript using the command(enscript is a tool that is used to convert a text file to PostScript and other formats): `enscript -2 -r -p psfile.ps textfile.txt`
- To convert a text file to PostScript (saved to psfile.ps): `enscript -p psfile.ps textfile.txt`
- To convert a text file to n columns where n=1-9 (saved in psfile.ps): `enscript -n -p psfile.ps textfile.txt`
- To print a text file directly to the default printer: `enscript textfile.txt`
- To convert a pdf to post-script: `pdf2ps file.pdf` or `pdftops original.pdf converted_name.ps` or `convert original.pdf converted_name.ps`
- To convert a post-script to pdf: `ps2pdf file.ps` or `pstopdf original.ps converted_name.pdf` or `convert original.ps converted_name.pdf`
- To merge the two documents first.pdf and second.pdf to output.pdf: `qpdf --empty --pages first.pdf second.pdf -- output.pdf` or `pdftk first.pdf second.pdf cat output output.pdf`
- To write only pages 1 and 2 of original.pdf to new.pdf: `qpdf --empty --pages original.pdf 1-2 -- new.pdf` or `pdftk A=original.pdf cat A1-2 output new.pdf`
- To rotate page 1 of original.pdf by 90 degrees clockwise to rotated.pdf: `qpdf --rotate=+90:1 original.pdf rotated.pdf`
- To rotate all pages of original.pdf 90 degrees clockwise and save to rotate-all.pdf: `qpdf --rotate=+90:1-z original.pdf rotated-all.pdf` or `pdftk A=original.pdf cat A1-endright output new.pdf`
- To encrypt with 128 bits public.pdf with the passwd mypw with output as private.pdf: `qpdf --encrypt mypw mypw 128 -- public.pdf private.pdf` or `pdftk public.pdf output private.pdf user_pw PROMPT`
- To decrypt private.pdf with output as file-decrypted.pdf: `qpdf --decrypt --password=mypw private.pdf file-decrypted.pdf`
- To open a pdf(evince is a pdf viewing GUI): `evince xyz.pdf`
- CUPS interface is available at: `http://localhost:631`
