---
title: PC commands and short cuts (WIP)
date: 2025-01-17
tags:
  - skill
  - tech
---

1. **Google colab** short-cuts
	- to move cell up : `ctrl+m K`
	- to move cell down : `ctrl+m J`
	- to create a new cell below : `ctrl+m b`
	- to create a new cell above : `ctrl+m a`
	- to delete a cell : `ctrl+m d`
	- to convert a text cell to code cell : `ctrl + m + y`
	- to convert a code cell to text cell : `ctrl + m + m` (double tap m)
	- to replace within cell : `ctrl + shift + h`
	- to replace within entire notebook : `ctrl + h`
	- to run all cells : `ctrl + F9`
	- we can run shell commands by prefixing them with an exclamation mark ( ! )
		- or simply open a terminal in "new"
	- 

2. **Windows** Short-cuts
	1. "winver" in search box to check your windows version.
	2. Screen shot : Windows key + Shift + S
	3. clip-board :  Windows logo key + V.
	4. Windows + R to open "Run"
	5. Windows + R then type CMD. to open CMD or bash
	6. To check disk partition : `Win + R`, type `diskmgmt.msc`
		1. in cmd : check partition, remove them and combine them. 
		```
		diskpart
		list disk
		select disk X  (replace X with your SD card number from the list)
		clean
		create partition primary
		format fs=fat32 quick  (or exFAT if needed)
		assign
		exit
		```
		

3. **Linux / Bash**  commands
	1. check the number of lines inside a folder `ls /path/to/your/folder | wc -l`
	2. delete all the files which contains specific "string"  in their name.`rm *string*`
		1. use above command with caution. better first check it by using `ls *string*`
	3. Checking Disk Usage `df -h`
		- df : Disk Filesystem
		- -h : human readable form, MB, GB
	4. Open some specific folder from bash.
		- first `cd` to that folder
		- use `xdg-open .`
	5. 