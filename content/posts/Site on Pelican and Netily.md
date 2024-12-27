

---
title: "Site on Pelican and Netily"
date: "2024-12-18"
tags: 
- Tech
- Skill
---

helpful blog : https://iwanttoreadmore.com/blog/create-minimal-static-website-pelican/

1. open netlify [https://www.netlify.com]
	1. make your id on netlify. use free version
	2. Add new site > deploy manually
	3. it'll ask for drag and drop. leave this tab as it is for now.

2. open pelican documentation for reference [https://docs.getpelican.com/en/latest/index.html]
	1. go on quick start, read if you want or follow following command.
```bash
pip install pelican markdown
```

3. open file explorer. 
		1. create a folder with your project / website name and open that folder
		2. open cmd inside that folder.  run this command  "pelican-quickstart"
		3. it'll open some dialogues. answer them accordning to follow

> Where do you want to create your new web site? [.] .
   What will be the title of this web site? any name
>Who will be the author of this web site? any name
   What will be the default language of this web site? [en] en 
   Do you want to specify a URL prefix? e.g., https://example.com (Y/n) n
> Do you want to enable article pagination? (Y/n) n 
> What is your time zone? [Europe/Paris] Asia/Colombo
> Do you want to generate a tasks.py/Makefile to automate generation and publishing? (Y/n) Y 
> Do you want to upload your website using FTP? (y/N) n 
> Do you want to upload your website using SSH? (y/N) n 
> Do you want to upload your website using Dropbox? (y/N) n 
> Do you want to upload your website using S3? (y/N) n 
> Do you want to upload your website using Rackspace Cloud Files? (y/N) n 
> Do you want to upload your website using GitHub Pages? (y/N) n

4. it'll create some files in your project folder.
	1. but before moving forward we need to create an article. in markdopwn format.
	2. go to content folder and create a file "first.md". and write these few lines first
```txt
Title: First Document
Date: 2024-12-22 13:37
Category: Home

This is the first page I am ceating for test.
```

5. 
> you can skip this step if you want. It's for adding a simple theme.
> create a folder themes. inside it one more folder "name of theme", inside it 2 folders static and templates
> inside static : css and images
>inside css you can have your css file which will have style stuff.
>`add some css file link here
>
>now go inside templates, create a file base.html
>and add some basic template in it
>`add one example
>

6. Now you have a page in content folder, output folder is empty, some stuff in themes folder, and 4 other files. ignore them for now.
7. open your cmmd in project folder and "if you skipped step 5" then run this command. `pelican content ` now check your output folder and you will find some html pages generated.
8. if you acted on step 5 and created your own theme then you need to run this command `pelican content -s pelicanconf.py -t /projects/your-site/themes/your-theme`. check your pages in output folder.
9. Maybe you will not like theme or template. Then you can change it in your Theme folder. as mentioned in step 5.
10. now go back to that netlify tab which we left opened in step 1.3. Now you have created output folder in your local PC, just drag and dropeed it here. after little wait, now you can see preview. It'll give you some random URL, you can change it in "Site configration"..
11. Congratulations you have completed your first website and hosted it on internet. For adding a new page. use step 4, 7 or 8.
12. now go to netlify > Sites (check right pan) > pick your site > click on Deploys, you will see empty space and "drag and drop / upload / browse", just drag and drop your whole output folder here. 
13. Done. muhahhahaha 🔥🔥🔥🔥