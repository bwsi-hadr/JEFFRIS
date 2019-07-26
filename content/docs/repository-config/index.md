---
title: 'Repository Configurations'
date: 2019-02-11T19:27:37+10:00
draft: false
weight: 3
---

## Add the Upstream

To properly set up your github repositories, you will need to set the MIT code repositories as your upstreams. While the origin repository represents code that you write, the upstream repository is the original repostiory that your code "works off of." At first, it may seem like you don't need to use the upstream anymore, since you already have the code. However, this is an important step because if the upstream code changes, adding the upstream allows you to update your code to match the most recent state of the upstream.

1. Open a terminal and go to the directory of your image processing repository. Then, type the command `git remote -v` to check that your origin is set properly. You should see the following output:
	```
	origin	https://github.com/<username>/student-image-processing (fetch)
	origin	https://github.com/<username>/student-image-processing (push)
	```

2. Add the upstream by writing the following line into your terminal:
	```
	git remote add upstream https://github.com/bwsi-hadr/student-image-processing.git
	```
	This now makes the bwsi-hadr repository **(not your own)** the upstream repository for your work.

3. Check that you've successfully added your upstream by trying the command `git remote -v` again. You should see the following output:
	```
	origin	https://github.com/<username>/student-image-processing (fetch)
	origin	https://github.com/<username>/student-image-processing (push)
	upstream	https://github.com/bwsi-hadr/student-image-processing.git (fetch)
	upstream	https://github.com/bwsi-hadr/student-image-processing.git (push)
	```

	![Code here](/JEFFRIS/git-remote-v-add-upstream.gif)

4. Repeat steps 1-3 for all three repositories: student-image-processing, student-access-images, and student-pi-imaging

5. Check that all three of your repositories are set with _your repository_ as the origin and the _bwsi-hadr repository_ as the upstream.

	![Code here](/JEFFRIS/git-remote-v-double-check.gif)

	The command `clear` in a Linux command line clears the terminal, similar to the clear button on a calculator. The command is completely optional and does not affect the repositories. <br />
	**Please Note:** Your origin should have your username, not intermezzio, as the owner of each repository. Also, if any of the information in your `git remote -v` output is incorrect, use <br />
	```git remote set-url [origin or upstream] the-correct-url.com/something.git``` <br />
	to fix your links.

## Set up your Submodule

Submodules are an important feature for larger git projects. Instead 

1. 