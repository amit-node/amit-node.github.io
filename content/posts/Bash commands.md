---
title: Bash Commands
date: 2025-04-02
tags:
  - tech
---
1. `echo` is like print command in python
2. `cd` change directory.
	1. `cd ..` parent directory
	2. `cd ~` Home directory
	3. `cd -` previous directory
3. Renaming a file `mv a b`
4. check the number of files + folders inside a folder `ls /path/to/your/folder | wc -l`
	1. `wc -l` command in Bash is used to count the number of lines in a file or output `wc -l filename.txt`
	2. for only files, excluding subfolders `find path/to/folder -type f | wc -l`
	3. for everything `find path/to/folder | wc -l`
	4. Count Files in the Current Directory (Non-Recursively) : `ls -1 | wc -l`
5. delete all the files which contains specific "string"  in their name.`rm *string*`
	1. to remove directories you need to use `rm -r *string*` , in fact this command will remove all folder and files with this string.
	2. use above command with caution. better first check it by using `ls *string*`
6. Checking Disk Usage `df -h`
	- df : Disk Filesystem
	- -h : human readable form, MB, GB
7. Space occupied `du -h`
	1. find size of all folders in the current folder ? `du -sh */`
	2. some specific folder `du -sh /path/to/folder`
	3. find size one specific file `du -h filename.txt`
8. Create a virtual environment: `python -m venv venv` or python3
	1. Activating on windows `venv\Scripts\activate`
	2. Activating on Linux  `source venv/bin/activate`
	3. deactivating `deactivate`
9. Copy a folder with all content inside it. `cp -r path/to/source_folder path/to/destination_folder`
	1. How to copy 3 folders from one directory to another directory. these folders have many subfolders and files. `cp -r /source_directory/folder1 /source_directory/folder2 /source_directory/folder3 /destination_directory/`
10. Stopping an ongoing process in terminal `ctrl + c`
	1. If `Ctrl + C` doesn’t work (some processes ignore this signal),
		1. Use `ps aux | grep process_name` to find the PID of the process you want to stop. Replace `process_name` with the name of your command or script.
		2. Once you have the PID, you can use the `kill PID` command.
		3. If it still doesn’t terminate, try forcing it with: `kill -9 PID`
			1. This `-9` option sends a SIGKILL signal, forcing the process to stop immediately.
11. Removing a non-empty directory forcefully `rm -rf /path/to/directory`
12. Clearing cache in python `pip cache purge`
13. to check past commands `history`
	1. to check past n commands `history n`
14. zip a folder as .zip `zip -r output.zip folder_name`
15. Zip a tar file `tar -czvf archive_name.tar.gz directory_name`
- **`-c`** Creates a new archive. 
- **`-z`** Compresses the archive using gzip.
- **`-v`** Shows the progress of the archiving (optional).
- **`-f`** Specifies the filename of the archive.
	1. Exclude certain files `tar --exclude="*.log" -czvf my_directory.tar.gz my_directory`
	2. unzip a .tar.gz file`tar -xzvf file.tar.gz`
	3. If you want to extract the contents to a specific directory, use the `-C` option `tar -xzvf file.tar.gz -C /path/to/directory`
16. To read a text file in Bash 
	1. Displays the entire content of the file.`cat filename.txt`
	2. Allows you to scroll through the file one screen at a time.`less filename.txt`, `more filename.txt`
	3. Displays the first few lines (default is 10 lines).`head filename.txt`.
	4. To specify a different number of lines, use `head -n 5 filename.txt`
	5. Displays the last few lines `tail -n 5 filename.txt`
17. Reading binary file in bash, first few lines `hexdump -C your_file.ext | head`
18. Check all running processes in the server `ps aux`
19. checking the task manager in bash `top`
	1. press `q` to exit
	2. `jobs` for background tasks
	3. 
20. Large transfer and Synchronization `rsync -avz username@server:/path/to/remote/folder /path/to/local/folder`
	- `rsync` is efficient for transferring large or complex directory structures as it only transfers changes.
	- a: Archive mode (preserves permissions and timestamps).
	- v: Verbose (shows detailed output).
	- z: Compresses the data during transfer.
21. I have a txt file. that txt file have many lines. I want to print each 6th line. like 1, 7, 13. how to do it in bash. single command `awk 'NR % 6 == 1' yourfile.txt`
22. Git commands
	1. clone ``
23. Finding a specific folder inside a folder recursively. `find <search_directory> -type d -name <target_folder_name>`
	1. Limit Search Depth: To search only up to a certain depth: `find /path/to/search -type d -name "target_folder" -maxdepth 3`
24. List all installed package by pip `pip list`
25. 











> 2024 done from chatgpt