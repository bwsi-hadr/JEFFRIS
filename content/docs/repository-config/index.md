---
title: 'Repository Configurations'
date: 2019-02-11T19:27:37+10:00
draft: false
weight: 3
---

## Add the Upstream

To properly set up your github repositories, you will need to set the MIT code repositories as your upstreams.

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