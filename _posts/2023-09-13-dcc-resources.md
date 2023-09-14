---
layout: post
title: Duke Computing Resources
date: 2023-09-13
tags: dcc for-dukies
categories: computing
---

<h3> Duke Computing Resources- An Overview </h3>

- DSS Studio Server: [http://knight.stat.duke.edu:8787/](http://knight.stat.duke.edu:8787/)
	
	- Can switch between knight, rook, algebra2, and others. Someone please tell me the difference between these!

- OIT [virtual machine](https://vcm.duke.edu/): helpful if the dss Studio server is crashing, or for using other languages.

- Duke Computing Cluster:

	- The [OIT DCC](https://oit-rc.pages.oit.duke.edu/rcsupportdocs/dcc/#getting-a-dcc-account) website is a super helpful resource.

	- You can check out an Rstudio server on the cluster. Information [here](https://oit-rc.pages.oit.duke.edu/rcsupportdocs/OpenOnDemand/RStudio/). The DCC OnDemandlogin site is [dcc-ondemand-01.oit.duke.edu](dcc-ondemand-01.oit.duke.edu).

	- If you aren't able to log on to any of these DCC resources, you might need to request access. Check [rtoolkits](https://rtoolkits.web.duke.edu/) to see if you have access. 

<h3> Duke Computing Cluster- The Basics </h3>

Simple steps to use the cluster through your terminal and use slurm:

1. To log-on, execute the following in the terminal

	``` 
	ssh NETID@dcc-login.oit.duke.edu
	```

2. Navigate to your desired working directory. Details [here](https://oit-rc.pages.oit.duke.edu/rcsupportdocs/dcc/files/#logging-into-the-dcc_1) on the differences between the various directories. I tend to use the following

	```
	cd /hpc/group/LAB/NETID
	```

3. Add/remove files with `git` or by using `sftp`:

	- Replace `ssh` with `sftp` upon login. Note that tab-complete often doesn't work well when in an `sftp` environment. 

	- To upload files <b> from your computer to the cluster</b>, execute `get FILENAME`.

	- To download files <b> from the cluster to your computer</b>, execute `put FILENAME`.

	- Some useful options: `-r` for working with directories, `-C` for working with large files

4. Life is easier if you can edit files with emacs (or similar) in the terminal.  To use emacs, open a file by executing `emacs FILENAME`. 

	- If you're going to be using a text editor in the terminal, I recommend doing a hot key tutorial. 

	- Some useful emacs commands: <b> C-x C-s </b> to save changes, <b> C-x C-c </b> to exit emacs

5. Submit a job to slurm by executing the following (see DCC website for helpful resources on setting up your .sh file)

	```
	sbatch NAME.sh
	```

check on the status of your jobs:

	```
	squeue -u NETID
	```

and to cancel jobs use `cancel JOB##`.




