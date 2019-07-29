---
title: 'Git Workflow'
date: 2018-11-28T15:14:39+10:00
weight: 4
---

## Summary

Git is a very efficient program that helps manage project development. Although it may seem complicating at first, all of its features are designed so you can easily track versions and work in parallel with others. The following tasks are done after code is edited to share that code with others. 

### Staging files

With git, changes to code are sent in "commits". Commits state what files are changed and how. To prepare a commit, you need to stage files (get them ready) for committing. In git, use the command `git add <file>` to stage a file for committing. To stage all files in a directory, use the following:
```
git add .
```
The opposite of this, removing a file, can be done with `git rm <file>`.

### Commits 

Now that files are staged, they need to be committed. In git, use the command `git commit` to make a commit. The best way to make a commit with a good message, however, is with the `-m` flag. This allows you to make a commit message, usually saying what you changed in the commit. For example, a good commit may look like the following:
```
git commit -m "Complete the NDVI image processing script."
```
Take note of a couple of things from the commit
* The commit message is specific
* The commit message uses the imperative tense

Some companies ensure specific formats for commit messages, but for the purpose of this project, you can make commit messages however you would like. Still, I would advise making content related commit messages (ex don't make your git commit message "hi").

If you want to combine your add and commit command, use the `-a` flag. For example:
```
git commit -am "Your commit message"
```
This command stages the files and commits them all at once.

**Please Note:** two flags, `-a` and `-m`, are combined to make the flag `-am`.
### Push

Now that the commit is made, it needs to be published, or pushed, to the origin (cloud) repository. To push your code, use the following command:
```
git push <location> <branch>
```
For this project, the location is always the origin, although when you pull code, you may need to pull from the upstream. The default branch is the master branch, and for this project, you will not need to use anything other than the master branch for pushing code. Consequently, your push commands will usually be
```
git push origin master
```
If this does not work on your computer, the origin has probably changed since you last updated your code. Pull your code first, then try again.

### Pull

Pulling code allows you to update your files based on other people's commits. Pull commands are done using the same format as pull commands, as shown:
```
git pull <location> <branch>
```
For example, in this project, most of your pull commands will look like the following:
```
git pull origin master
```
For push and pull commands, the default location and branch are origin and master, respectively. Because of this, the above command (as well as the push command) can be simplified to the following:
```
git pull
```
If the git pull does not work, check out the git merge section.

### Merge

Imagine two people, Alice and Bob, are making a painting. Alice and Bob leave the painting half-completed in a small room in their house. However, they both take pictures of the painting and print them out so they can look at the painting on their own. Alice has a great idea for the painting. She paints a few strokes onto her printed photo, then goes to the main painting to update it with her idea. Bob also has a great idea for the painting, and he paints a few strokes on his own photo. However, when Bob approaches the shared painting to make his updates, he realizes that the painting has changed since he's last viewed it. To fix his problem, Bob copies (pulls) Alice's edits onto his own photo, and then he merges Alice's ideas with his own ideas for changing the painting. Once Bob has successfully combined (merged) both edits to the painting, he updates (pushes) his changes on the shared painting.

I sincerely hope you enjoyed this metaphor about git merges. In the story, Bob experienced a merge conflict because two people tried to edit the same painting. He had to copy the edits to his personal photo before he could merge his edits and update the real painting. 

When you have an error pushing code because the origin has changed, you first have to pull your code.
```
git pull
```

If you are asked to write a commit message, you can skip the next step. If not, you may have a merge conflict. Your edits and your teammates' edits overlap. Now, open your repository in a program like [Sublime Merge](https://www.sublimemerge.com/) to see the conflicts.

Once you have merged the files, choosing how to combine the two (or more) commits, commit and push your changes.

![Code here](/JEFFRIS/git-push-pull-push.gif)

The above gif shows a possible merge conflict in the instructors' code (image-processing). I updated a python script on my computer, and the origin had an updated README. The automatic merge updated both files because the edits did not overlap.

# Troubleshooting