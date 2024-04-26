---
tags:
  - knowledge
  - ics53
aliases:
---
# ✒️Definition: 


# 🎞️Resource: 

# 😅Questions:
==every task/question needs a deadline to take an action==
- [ ] 
# ✨Takeaways:
1. when making the shell, make sure understand how background work, then write the code for shell 

# 🎢Journey:

# ⚙️Concept break down:
1. when shell is executing a a.out, the shell will clone itself, and make a.out possess the clone shell, 
	1. shell need to re-prompt the user for input after a execute terminate 
	2. fork -> execve()
2. the the execve ins foreground process, then the shell need to wait until the process dead, need waitpaid 

parent will return the pid of child, while child return 0 

## background:
1. allows for more child, 
2. need be alert to clean the zombie children
	1. the process of alert is call signal 

## signal: ECF (exception control flow )🫠
asynchronous process, 
maintain the signal in a bit vector, to let the process know there is asynchronous event happen 
ctrl c is just raise a flag in process it may not kill the process immediately, 
some signal can be ignore but some cannot be overwritten or ignore like 9, kill the process

the termination of the child can depends on the process group id, it can kill multiple processes. 

pnb = pending & ~ block, to get the bits to process 
signal take one integer argument,, convention, the argument are not ncessarily to be used. 
# ⚒️Implementation: 
