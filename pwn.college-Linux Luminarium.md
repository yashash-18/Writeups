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
**In this challenge, ```/challenge/run``` will write a copy of the flag to any file you specify as an argument on the commandline, with these constraints:** <br>
**>> Your argument must be an absolute path.** <br>
**>> The path must be inside your home directory.** <br>
**>> Before expansion, your argument must be three characters or less..** <br>
### Soln:
**-> First check in which directory u are... and if u are not in ```/home``` directory then navigate there using ```cd ../```** <br>
**-> And before that just create a file with a single character(any alphabet named file) named in ```/home/hacker``` where u have the access to create a file, as we need to copy the content from ```/challenge/run``` to a file which is less than three characters..** <br>
**-> Run ```/challenge/run ~/s``` and get the flag** <br>
<img width="1217" height="657" alt="image" src="https://github.com/user-attachments/assets/fb0957e8-7929-4154-8863-ed396f49446c" /><br><br>

# Comprehending Commands
## cat: not the pet, but the command!
### GOAL:
**There is a file named "flag" in the current directory and we need just to read it.** <br>
### Soln:
**-> Run ```ls``` to view the files that are present and run ```cat flag``` to read the content of that file** <br>
<img width="1197" height="660" alt="image" src="https://github.com/user-attachments/assets/74b879c7-53f2-4299-abc5-c5f34250f36c" /><br><br>

## catting absolute paths
### GOAL:
**There is a file named "flag" in a specific directory and we need just to read it but we cant access that file directly..** 
### Soln:
**-> Run ```ls``` to view the files that are present and run ```cat /flag``` to read the content of that file as we cant access it directly but can read the content of it** <br>
<img width="1222" height="455" alt="image" src="https://github.com/user-attachments/assets/af563e74-a9db-42d5-945e-122faa2883b7" /><br><br>

## more catting practice
### GOAL:
**In this level, the flag is in some crazy directory, and will not allow us to change directories with "cd", so no cat flag for us. we must retrieve the flag by absolute path, wherever it is...** <br>
### Soln:
**-> As there is path being displayed and we can run ```cat ../../path``` and get the flag** <br>
<img width="1211" height="225" alt="image" src="https://github.com/user-attachments/assets/0873001c-8463-428d-ac25-ed7f4c516ed8" /><br><br>

## grepping for a needle in haystack
### GOAL:
**In this challenge, I've put a hundred thousand lines of text into the /challenge/data.txt file. grep it for the flag!** <br>
**HINT: The flag always starts with the text "pwn.college"**
### Soln:
**-> Run ```grep pwn.college /challenge/data.txt``` and get the flag** <br>
**-> We use grep to return the lines that are containing that word** <br> 
<img width="1226" height="402" alt="image" src="https://github.com/user-attachments/assets/ad0382a0-73f5-4b5d-899c-940453013dcd" /><br><br>

## comparing files
### GOAL:
**In this challenge There are two files in ```/challenge```**
**>>```/challenge/decoys_only.txt``` contains 100 fake flags** <br>
**>>```/challenge/decoys_and_real.txt``` contains all 100 fake flags plus the one real flag** <br>
**We need to Use ```diff``` to find what's different between these files and get your flag!** <br>
### Soln:
**-> Navigate to ```/challenge``` and then run ```diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt``` and get the flag** <br>
<img width="1227" height="660" alt="image" src="https://github.com/user-attachments/assets/e6210f9d-3aa5-45e2-8d8f-afd450246234" /><br><br>

## listing files
### GOAL:
**In this challenge, we've named ```/challenge/run``` with some random name! List the files in "/challenge" to find it. Then invoke the discovered absolute path to get the flag.**
### Soln:
**-> Navigate to ```/challenge``` and list the files present in it using ```ls``` and then execute that file using ```./```** <br>
<img width="1196" height="676" alt="image" src="https://github.com/user-attachments/assets/fcb9df0b-dccf-4fb2-95e1-ef091f3beb4a" /><br><br>

## touching files
### GOAL:
**In this challenge we need to create two files: ```/tmp/pwn``` and ```/tmp/college```, and run ```/challenge/run``` to get the flag!**
### Soln:
**-> Just create two files in the ```/tmp``` directory using ```touch``` command and then run ```/challenge/run``` to get the flag** <br>
<img width="1195" height="507" alt="image" src="https://github.com/user-attachments/assets/2d7751b7-115e-4e46-99ae-8628d8935f1d" /><br><br>

## removing files
### GOAL:
**This challenge will create a "delete_me" file in your home directory! Delete it, then run ```/challenge/check```, which will make sure you've deleted it and then give you the flag!** 
### Soln:
**-> Run ```rm delete_me``` and then execute ```/challenge/check``` to get the flag** <br>
<img width="1202" height="601" alt="image" src="https://github.com/user-attachments/assets/7cf9e658-d0da-44e7-995c-b3b97950adf8" /><br><br>

## moving files
### GOAL:
**We need to move the file ```/flag``` to a specific path mentioned ```/tmp/hack-the-planet```** <br>
### Soln:
**-> Run ```mv /flag /tmp/hack-the-planet``` and then execute ```/challenge/check``` to get the flag** <br>
<img width="1217" height="627" alt="image" src="https://github.com/user-attachments/assets/7e34bc30-cf22-435c-8ce2-b3931fe2fb73" /><br><br>

## copying files
### GOAL:
**This challenge wants you to copy the ```/flag``` file to ```/tmp/hack-the-planet```** 
### Soln:
**-> Run ```cp /flag /tmp/hack-the-planet``` and then execute ```/challenge/check``` to get the flag** <br>
<img width="1200" height="405" alt="image" src="https://github.com/user-attachments/assets/7100e273-9cd4-4fa9-8eae-33c5258d73d0" /><br><br>

## hidden files




















