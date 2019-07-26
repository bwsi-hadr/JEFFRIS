---
title: 'Task Management'
date: 2018-11-28T15:14:39+10:00
weight: 2
---

## Opening the Task Manager

A task manager is important for remotely managing your scripts on the Raspberry Pi. Because the Raspberry Pi has a weak processor, it is ideal to use a terminal based task manager to end unnecessary tasks, like scripts that have already completed.

1. After you SSH into the raspberry pi, open a terminal and write
	```
	ps aux
	```
	This will list all of the tasks running on the Raspberry Pi.

2. To search for a specific task (like a script), use the `grep` feature. The following line shows how you can search for all tasks with the name "python in them.
	```
	ps aux | grep python
	```
	The pipe ("|") tells the computer to take the output of `ps aux` and search for it using grep.

3. Once you've found the task, take the id of the task (a four digit number on the same line as the task name) and run the following code:
	```
	kill [####]
	```
	This ends that task.