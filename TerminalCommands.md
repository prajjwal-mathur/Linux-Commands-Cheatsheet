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