---
title: 'Download the Code'
date: 2019-02-11T19:27:37+10:00
weight: 2
---

There are three Github repositories for this project, as follows:
<table>
	<tbody>
		<tr><td>**Name**</td><td>**Link**</td><td>**Purpose**</td></tr>
		<tr>
			<td>student-image-processing</td>
			<td>https://github.com/bwsi-hadr/student-image-processing</td>
			<td>Process Images using Python and OpenCV, and show the analysis in Flask.</td>
		</tr>
		<tr>
			<td>student-access-images</td>
			<td>https://github.com/bwsi-hadr/student-access-images</td>
			<td>Use MongoDB to store Raspberry Pi images to a database, and create methods to open them in the Flask application.</td>
		</tr>
		<tr>
			<td>student-pi-imaging</td>
			<td>https://github.com/bwsi-hadr/student-pi-imaging</td>
			<td>Take time lapse images on the Raspberry Pi during flights.</td>
		</tr>
	</tbody>
</table>
<br />

## Creating Forks of the Repositories

1. Open the image processing repository above. On the page, click the 'Fork' button in the top right corner of the page. This will create a copy of the repository that you can use for writing your own code.

	![Image here](/JEFFRIS/github-fork-repository.png)

2. Now you should have a forked repository of student-image-processing. Make sure that you now have a repository on github with the following text:

	![Image here](/JEFFRIS/github-new-forked-repository.png)

	**Please note:** Your fork should be &lt;username>/student-image-processing, replacing my username (intermezzio).

3. Repeat steps 1-2 for all three repositories: student-image-processing, student-access-images, and student-pi-imaging.

## Cloning the Repositories to your Computer 

1. Open your _newly created repository_ for image processing (&lt;username>/student-image-processing). Now, press the 'Clone or download' button and copy the link. If you are not familiar with using git, make sure HTTPS is selected. If you want to clone using SSH, however, follow [this tutorial](https://help.github.com/en/articles/adding-a-new-ssh-key-to-your-github-account) to add SSH to your github account.

	![Image Here](/JEFFRIS/github-clone-repository.png)

2. Open a terminal (or git bash) on your computer and go to the directory where you want to place your repository. Then, type in the following command to clone (copy) the online repository to your computer:
	```
	git clone https://github.com/<username>/student-image-processing
	```
	![Code here](/JEFFRIS/git-clone-terminal.gif)

	The `git clone` command creates a folder on your computer with the same name as the online repository. All of the files are then copied into that folder. <br />
	**Please note:** You will not see the directory `student-access-images/` in your repository when you clone it. You will add that in a future tutorial.

3. Repeat steps 1-2 for all three repositories: student-image-processing, student-access-images, and student-pi-imaging.

4. When all three repositories are cloned (into separate folders), check that they all have the right files in them:

	![Code here](/JEFFRIS/git-clone-double-check.gif)