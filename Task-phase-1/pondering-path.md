# THE ROOT

1) OBJECTIVE- Invoke the program pwn located in the root directory
2) SOLUTION- Use the absolute path

&nbsp;

![command line screenshot!](snapshots\sc1.png)

&nbsp;

### EXPLANATION
The root directory, which may be accessed using /, is where the file system begins. / can be used to access the pwn application because it is situated in the root directory. Thus, the absolute path of the pwn file is /pwn. To execute an executable, just supply its path to the command line.

---
&nbsp;

# PROGRAM AND ABSOLUTE PATHS
1) OBJECTIVE- invoke the program present inside challenge directory inside root.
2) SOLUTION- give the command /challenge/run

&nbsp;

![](snapshots\sc2.png)

&nbsp;

### EXPLANATION
To find the flag first the challenge directory has to be accessed which is inside the root directory, so we use the /challenge/run path.

---
&nbsp;

# POSITION THY SELF
1) OBJECTIVE- Invoke the run program in the /challenge directory after changing the working directory.
2) SOLUTION- to use cd to change the current directory

&nbsp;

![](snapshots\sc3.png)

&nbsp;
### EXPLANATION
As I try to invoke the challenge directory, it gives the command to change the working directory. cd /var/lib/apt/lists changes the current directory to /var/lib/apt/lists as right before the $ sign. and after that as i try to invoke the /challenge directory , using /challenge/run it gives me the flag.

---
&nbsp;

# Position elsewhere
1) OBJECTIVE- Invoke the run program in the /challenge directory after changing the working directory.
2) SOLUTION- to use cd to change the current directory

&nbsp;

![](snapshots\sc4.png)

&nbsp;
### EXPLANATION
As I try to invoke the challenge directory, it gives the command to change the working directory. cd /proc/159 changes the current directory to /proc/159 as right before the $ sign. and after that as i try to invoke the /challenge directory , using /challenge/run it gives me the flag.

---
&nbsp;

# implicit relative paths, from /
1) OBJECTIVE- Invoke the run program in the /challenge directory after changing the working directory.
2) SOLUTION- to use cd to change the current directory
and then giving the relative path, in the / directoy as challenge/run.

&nbsp;

![](snapshots\sc5.png)

&nbsp;
### EXPLANATION
As I try to invoke the challenge directory, it gives the command to change the working directory to /. cd / changes the current directory to / as right before the $ sign. and after that as i try to invoke the /challenge directory , using /challenge/run it gives me the flag.

---
&nbsp;

# explicit relative paths, from /
1) OBJECTIVE- Invoke the run program in the /challenge directory after changing the working directory to /, and to use a relative path.
2) SOLUTION- to use cd to change the current directory
and then giving the relative path, in the / directoy as challenge/run.

&nbsp;

![](snapshots\sc6.png)

&nbsp;
### EXPLANATION
As I try to invoke the challenge directory, it gives the command to change the working directory to /.  cd / changes the current directory to / as right before the $ sign, but now we have to use relative path, so i put the command ./challenge/run, which gives me the flag. 


---
&nbsp;

# home sweet home
1) OBJECTIVE- Provide the run program with an argument which specifies where we want the flag to be copied to to.

&nbsp;

![](snapshots\sc8.png)

&nbsp;
### EXPLANATION
~ expands to /home/hacker. This is the default directory in which the shell opens to. ~/temp expands to home/hacker/temp which is the argument given to the run program. Next run is executed and it copies the flag to the temp file in ~ directory and displays it on command line. 