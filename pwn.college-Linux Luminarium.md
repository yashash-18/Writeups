# Hello Hackers
## Intro to Commands
### GOAL:
**Our goal is to invoke the hello command to get the flag** <br>
### Soln:
**-> Just type ```hello``` in the terminal and get the flag** <br>
<img width="1341" height="657" alt="image" src="https://github.com/user-attachments/assets/d02c472b-f447-4555-8530-8a163d45075c" /><br><br>

## Intro to arguments
### GOAL:
**In this challenge, to get the flag, we must run the hello command with a single argument of 'hackers'** <br>
### Soln:
**-> Just type ```hello hackers``` in the terminal and get the flag** <br>
<img width="1335" height="170" alt="image" src="https://github.com/user-attachments/assets/e7dd6257-399e-49b6-8492-c97cd8491f36" /><br><br>

## Command History
### GOAL:
**In this challenge, to get the flag just click on up arrow as mentioned that flag is stored in the command history which is already stored.** <br>
### Soln:
**-> Click on up arrow in the terminal and get the flag** <br>
<img width="1342" height="327" alt="image" src="https://github.com/user-attachments/assets/6bc6d247-6328-49a6-8632-3a3cd8fca653" /><br><br>

# Pondering Paths
## The Root
### GOAL:
**In this challenge, the flag is located at a specific path, which is provided in the challenge description. Simply navigate to that path and retrieve the flag.** <br>
### Soln:
**-> First check in which directory u are... and if u are not in ```/``` root directory then navigate there using ```cd ../..```** <br>
**-> It says that ```pwn``` is not a directory it contains bash script.. so try running as ```./pwn``` and get the flag** <br>
<img width="1342" height="582" alt="image" src="https://github.com/user-attachments/assets/2170039f-e730-418b-8584-f4de5c778aec" /><br><br>

## Program and Absolute Paths
### GOAL:
**We want to execute the ```run``` file that is in the ```challenge``` directory that is, in turn, in the ```/``` directory. If we invoke the challenge correctly, it will give you the flag.** <br>
**i.e, From the ```/``` root directory execute ```/challenge/run``` as mentioned and get the flag** <br>
### Soln:
**-> First check in which directory u are... and if u are not in ```/``` root directory then navigate there using ```cd ../..```** <br>
**-> Now run ```/challenge/run``` and get the flag** <br>
<img width="1335" height="385" alt="image" src="https://github.com/user-attachments/assets/41184f95-af6a-49c8-b7f0-c71f04ae4fc2" /><br><br>

## Position thy self
### GOAL:
**We need to execute the ```/challenge/run``` program from a specific path (which it will tell us). we need to do ```cd``` to that directory before rerunning the challenge program and then get the flag** <br>
**i.e, First we need to find the specific path and then execute it and get the flag** <br>
### Soln:
**-> First check in which directory u are... and if u are not in ```/``` root directory then navigate there using ```cd ../..```** <br>
**-> Now just try running ```/challenge/run``` and observed a path and now navigate there and try executing it and get the flag** <br>
<img width="1342" height="657" alt="image" src="https://github.com/user-attachments/assets/a3dfb18f-8502-4572-9ef0-1664b8a4a599" /><br><br>

## Position elsewhere
### GOAL:
**Same as the above but just it is being repeated 5 times** <br>
**i.e, Just find all the paths and at one specific path get the flag** <br>
### Soln:
**-> First check in which directory u are... and if u are not in ```/``` root directory then navigate there using ```cd ../..```** <br>
**-> Run ```/challenge/run``` and get the path which repeats for 5 times and then get the flag**<br>
<img width="802" height="620" alt="image" src="https://github.com/user-attachments/assets/ca883431-71d7-4bc1-b144-84446a6379d4" /><br><br>

## Implicit relative paths, from /
### GOAL:
**First we need to change our current working directory to ```/``` Then invoke ```/challenge/run``` using a relative path. but For this level, the relative path starts with the letter c** <br>
**So we need to find the relative path and then executes it** <br>
### Soln:
**-> First check in which directory u are... and if u are not in ```/``` root directory then navigate there using ```cd ../..```** <br>
**-> As they mentioned that the relative path starts with "c" i.e, if we want to access a file in ```/tmp/a/b``` and our cwd is ```/``` so the relative path is ```tmp/a/b```** <br> 
**-> Generally we try to run ```/challenge/run``` in root directory right but as they mentioned about relative path so now try running it with but without ```/```** <br>
<img width="1197" height="781" alt="image" src="https://github.com/user-attachments/assets/ce512318-9e37-4dd1-af6e-edf1dc88031a" /><br><br>

## Explicit relative paths, from /
### GOAL:
**First we need to change our current working directory to ```/``` Then invoke ```/challenge/run``` using a relative path. but For this level, the relative path starts with the letter ```.``` as it is said that explicit relative path** <br>
### Soln:
**-> First check in which directory u are... and if u are not in ```/``` root directory then navigate there using ```cd ../..```** <br>
**-> As they mentioned that the relative path starts with "." now in root directory try running ```./challenge/run``` and get the flag** <br>
<img width="1211" height="716" alt="image" src="https://github.com/user-attachments/assets/0fef16fb-cd47-4ba5-a972-8570cf0264a4" /><br><br>

## Implicit relative path
### GOAL:
**First we need to change our current working directory to ```/``` Then invoke ```/challenge/run``` , but For this level,  we have to launch run in ```/challenge```** <br>
### Soln:
**-> First check in which directory u are... and if u are not in ```/``` root directory then navigate there using ```cd ../..```** <br>
**-> Now navigate to ```/challenge``` and to run an executable file we use ```./``` so now run ```./run``` and get the flag** <br>
<img width="1227" height="711" alt="image" src="https://github.com/user-attachments/assets/c9d916ea-85ec-452f-a8bb-32064370c435" /><br><br>

## home sweet home
### GOAL:
**











