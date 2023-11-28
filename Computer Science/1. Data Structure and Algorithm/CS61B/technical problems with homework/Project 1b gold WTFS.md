1. git pull origin master does not work!!!
2. intelliJ reports "the file in the editor is not runnable"
	1. solution: file -> new -> project, remove original main, stick whatever you need inside.
3. intelliJ reports "package org.junit does not exist"
	1. right click pom.xml (you have to add one)
	2. select maven 
	3. reload project
		alternative:
		1. add framework support
			1. where to find: help -> action -> add framework support
		2. add marven
		3. okay
		==did not work==. problem unsolved.
	==project paused==