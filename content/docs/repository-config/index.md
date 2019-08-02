---
title: 'Repository Configurations'
date: 2019-02-11T19:27:37+10:00
draft: false
weight: 3
---

To properly set up your github repositories, you will need to set the MIT code repositories as your upstreams. While the origin repository represents code that you write, the upstream repository is the original repostiory that your code "works off of." At first, it may seem like you don't need to use the upstream anymore, since you already have the code. However, this is an important step because if the upstream code changes, adding the upstream allows you to update your code to match the most recent state of the upstream.

## Add the Upstream

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
	**Please Note:** Your origin should have your username, not intermezzio, as the owner of each repository. 

## Set up your Submodule

Submodules are an important feature for larger git projects. A submodule connects two repositories, which means that one repository is literally inside another. More information about submodules can be found [here](https://www.atlassian.com/blog/git/git-submodules-workflows-tips). In this project, you will make your `student-access-images` repository a submodule of your `student-image-processing` repository.

1. Open a terminal (or git bash terminal) on your computer and navigate to your `student-image-processing` project folder. You should have cloned this repository when you [downloaded the code](/JEFFRIS/docs/code-downloads).

2. **BE EXTREMELY CAREFUL** when you perform this next step. Make sure your **forked** `student-access-images` repository is set as the submodule, as opposed to the bwsi-hadr one. To add the submodule, run the following command in your `student-image-processing` repository:
	```
	git submodule add https://github.com/<username>/student-access-images.git
	```

3. Save your changes by typing the following code:
	```
	git add .
	git commit -m "Add the 'student-access-images' submodule"
	git push origin master
	```

4. Once these commands are run, open your `student-image-processing` repository on github and check that the submodule is added:
	
	![Image here](/JEFFRIS/github-submodule-added.png)

	The interesting folder icon in the image above is the submodule. The `@ 09d8a20` after the folder name is the last commit for `student-access-images` on this repository.

# Troubleshooting

## Troubleshooting the Upstream Setup

Also, if any of the information in your `git remote -v` output is incorrect, use <br />
```
git remote set-url [origin or upstream] the-correct-url.com/something.git
```
to fix your links

![Code here](/JEFFRIS/git-remote-set-url.gif)

## Troubleshooting the Submodule Setup

If you set the wrong repository as your submodule, follow the following steps to remove it.

1. Remove the actual folder. In the repository, running the following command will remove the folder:
	```
	rm -rf student-access-images
	```

2. Remove the `.gitmodules` file. This can be done by doing the following:
	```
	rm .gitmodules
	```

3. Then, open the file `config` in the `.git` folder and remove the lines that specify the submodule. This file can be opened with the following command:
	```
	nano .git/config
	```
	Now, you should be ready to add the submodule.
