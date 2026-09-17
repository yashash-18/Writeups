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










