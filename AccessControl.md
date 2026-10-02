# Access Control
## LAB-1: Unprotected admin functionality
### GOAL:
**This lab has an unprotected admin panel, To solve the lab we need to delete the user ```carlos```** 
### Soln:
<img width="755" height="330" alt="image" src="https://github.com/user-attachments/assets/471cd3d9-48e5-4219-bf37-bfd6453e8398" /><br>
**-> Access the lab and try searching for any paths or endpoints in order to get access to the admin panel** <br>
**-> Now try checking ```/robots.txt``` whether are there any paths that the web crawlers are not allowed to visit** <br>
<img width="236" height="75" alt="image" src="https://github.com/user-attachments/assets/92222028-219a-4a78-8a12-630bf4d3dab0" /><br>
**-> Found a path and now try to navigate their and explore it.** <br>
<img width="753" height="340" alt="image" src="https://github.com/user-attachments/assets/67433ac1-a907-448c-ad80-28ce515cf66f" /><br>
**-> Delete the user ```carlos``` and the lab is solved✅** <br><br>

## LAB-2: Unprotected admin functionality with unpredictable URL
### GOAL:
**This lab has an unprotected admin panel, It's located at an unpredictable location, but the location is disclosed somewhere in the application.** <br>
**To Solve the lab access the admin panel, and using it to delete the user ```carlos```**
### Soln:
<img width="1085" height="356" alt="image" src="https://github.com/user-attachments/assets/7ad9ad59-5648-488e-9054-1c3dfc91c48c" /><br>
**-> Access the lab and as they mentioned that the location is disclosed somewhere in the application, so try inspecting the page source to retrive any information** <br>
<img width="627" height="212" alt="image" src="https://github.com/user-attachments/assets/b4afbbc0-3b26-4749-9900-1f068fc36225" /><br>
**-> Found a path and now try navigating there explore it** <br>
<img width="891" height="326" alt="image" src="https://github.com/user-attachments/assets/a49c920d-eb8f-44f3-b89c-54553828a847" /><br>
**-> Delete the user ```carlos``` and the lab is solved✅** <br><br>

## LAB-3: User role controlled by request parameter
### GOAL:
**This lab has an admin panel at ```/admin```, which identifies administrators using a forgeable cookie.**<br>
**To Solve the lab delete the user ```carlos``` and log in to your own account using the following credentials: ```wiener:peter```** 
### Soln:
<img width="990" height="411" alt="image" src="https://github.com/user-attachments/assets/a8ab73b8-2a3b-49d1-b136-47c615a86643" /><br>
**-> Access the lab and log in to your acc with the given credentials** <br>
**-> Now inspect the page and view all the cookies as they mentioned that there is a forgeable cookie which identifies administrators** <br>
**-> Initially for the key "Admin" it is "false" as we can modify it now change it to "True" and explore that in a new tab** <br>
<img width="1630" height="392" alt="image" src="https://github.com/user-attachments/assets/34341dfe-2617-432d-a124-11b7b6968f1d" /><br>
**->Got the admin panel after adding the ```/admin``` to that url** <br>
<img width="782" height="331" alt="image" src="https://github.com/user-attachments/assets/5084ff3a-daf6-4f82-a9d2-e029d6c754f4" /><br>
**-> Delete the user ```carlos``` and lab is solved✅** <br><br>

## LAB- 5: URL-based access control can be circumvented
### GOAL:
**This website has an unauthenticated admin panel at ```/admin```, but a front-end system has been configured to block external access to that path. However, the back-end application is built on a framework that supports the ```X-Original-URL``` header** <br>
**To solve the lab, access the admin panel and delete the user ```carlos```** <br>
### Soln:
<img width="1036" height="452" alt="image" src="https://github.com/user-attachments/assets/683908cf-3639-4a0d-a926-dcc19c9e8933" /><br>
**-> Access the lab and inspect this in burpsuite** <br>
**-> Now click on admin panel and send it to repeater and then as mentioned that front-end system has been configured to block external access to that path, so now place the header ```X-Original-URL:/admin``` and check the response of it..** <br>
<img width="1566" height="560" alt="image" src="https://github.com/user-attachments/assets/a72ccc68-8b14-495f-96b5-823ed86721e6" /><br>
**-> Now when we try to delete the user from the header itself the response says that missing parameter which means it isn't defined here so lets try to give ```?username=carlos```in the main query and ```/admin/delete``` in the header** <br>
**-> Delete the user ```carlos``` and lab is solved✅** <br><br>




