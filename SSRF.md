# SSRF
## LAB-1: Basic SSRF against the local server
### GOAL:
**This lab has a stock check feature which fetches data from an internal system.** <br>
**To solve the lab, change the stock check URL to access the admin interface at ```http://localhost/admin``` and delete the user ```carlos```** <br>
### Soln:
<img width="1096" height="327" alt="image" src="https://github.com/user-attachments/assets/87f53a31-d4eb-43be-8868-d3a54a0ff432" /><br>
**-> After accessing the lab view details of either of the item and we can see a option like ```check stock``` which fetches data from an internal system.** <br>
<img width="1157" height="837" alt="image" src="https://github.com/user-attachments/assets/920289d3-13c6-4113-90a3-80851f872f74" /><br>
**-> Now copy the request and inspect it in the "burpsuite" and turn on the ```intercept``` and then click on "check stock" and now send the request to ```repeater``` and check the response of the requests** <br>
<img width="765" height="332" alt="image" src="https://github.com/user-attachments/assets/0f3f4646-c9be-4c02-8591-4d449632cdc5" /><br>
**-> As mentioned that "change the stock check URL to access the admin interface" and we observer ```stockApi``` is framing a url , so now lets change the url to "http://localhost/admin" and check the response** <br>
<img width="1571" height="377" alt="image" src="https://github.com/user-attachments/assets/cb098d98-3476-4672-a80d-24463fdc9983" /><br>
**-> Got the admin interface and now modify it in order to delete the ```carlos``` user i.e, ```http://localhost/admin/delete?username=carlos```** <br>
**-> The user got deleted and the lab is solved✅** <br><br>

## LAB-2: Basic SSRF against another back-end system
### GOAL:
**This lab has a stock check feature which fetches data from an internal system.** <br>
**To solve the lab, use the stock check functionality to scan the internal ```192.168.0.X``` range for an admin interface on port 8080, then use it to delete the user carlos.** <br>
### Soln:
<img width="1267" height="425" alt="image" src="https://github.com/user-attachments/assets/06c089db-77bc-4a45-9978-cce2aea0f8b6" /><br>
**-> After accessing the lab view details of either of the item and we can see a option like ```check stock``` which fetches data from an internal system.** <br>
<img width="1157" height="837" alt="image" src="https://github.com/user-attachments/assets/920289d3-13c6-4113-90a3-80851f872f74" /><br>
**-> Now copy the request and inspect it in the "burpsuite" and turn on the ```intercept``` and then click on "check stock" and now send the request to ```intruder``` first as we don't know the exact ip addr..so add ```{}``` to "x" in ```192.168.0.{x}:8080/admin``` and then start the attack by giving payload as only numbers from "1-254" and start the attack** <br>
<img width="1886" height="437" alt="image" src="https://github.com/user-attachments/assets/03d94bb0-2846-4e51-8cf8-d7ea9d8af4b7" /><br>
**-> Now check if it returns "200" then send that request to repeater and then frame the url as ```http://192.168.0.x:8080/admin/delete?username=carlos``` where x is already submitted when u send the request to repeater.** <br>
<img width="1401" height="302" alt="image" src="https://github.com/user-attachments/assets/41f0b13f-bfc5-4db9-8f02-199e7baf6c42" /><br>
**-> The user got deleted and the lab is solved✅** <br><br>

## LAB-3: SSRF with blacklist-based input filters
### GOAL:
**To solve the lab, we need to change the stock check URL to access the admin interface at ```http://localhost/admin``` and delete the user ```carlos``` but The developer has deployed two weak anti-SSRF defenses that you will need to bypass..** <br>
**Our main goal is to find the two anti-SSRF defenses and bypass it..** <br>
### Soln:
<img width="1192" height="392" alt="image" src="https://github.com/user-attachments/assets/10bdeb88-7607-4261-94d0-1392cd9be0a6" /><br>
**-> After accessing the lab view details of either of the item and we can see a option like ```check stock``` which fetches data from an internal system.** <br>
**-> Now copy the request and inspect it in the "burpsuite" and turn on the ```intercept``` and then click on "check stock" and now send the request to ```repeater```  and try the url that was mentioned ```http://127.0.0.1/admin```** <br>
**-> It displays that ```External stock check blocked for security reasons``` which means that it is blocking "127.0.0.1" so we need to bypass that first**<br>
<img width="1242" height="377" alt="image" src="https://github.com/user-attachments/assets/6382d804-a371-4229-93ad-4708853fb533" /><br>
**-> We can use "127.1" instead of 127.0.0.1 and then check the response... and observed that it return ```200``` ok which has been bypassed** <br>
**-> Now try inserting ```http://127.1/admin``` which still blocks i.e, it blocks /admin.. but as we read that "Obfuscate blocked strings using URL encoding or case variation" which means that "A character can be represented using its percent-encoded form"(/%61->a i.e, /%61dmin) or "Case Variation" which mean we can change "capitalization"(/Admin or /ADMIN)** <br>
<img width="1526" height="396" alt="image" src="https://github.com/user-attachments/assets/242549b4-9229-40ea-9ba6-05ef1aedd3ab" /><br>
**-> After inserting ```http://127.1/Admin``` it return ```200 ok``` and we can observe the admin interface.. and now insert ```http://127.1/Admin/delete?username=carlos```** <br>
**-> The user got deleted and the lab is solved✅** <br><br>

## LAB-4: SSRF with filter bypass via open redirection vulnerability
### GOAL:
**To solve the lab, we need to change the stock check URL to access the admin interface at ```http://192.168.0.12:8080/admin``` and delete the user ```carlos```**<br>
**Our main goal is to find the redirect endpoint that lets you control where the local application sends the request** 
### Soln:
<img width="1292" height="342" alt="image" src="https://github.com/user-attachments/assets/f336c5b8-68d4-46b6-9ed3-40b3f39923f0" /><br>
**-> After accessing the lab view details of either of the item and we can see a option like ```check stock``` which fetches data from an internal system.** <br>
**-> Now copy the request and inspect it in the "burpsuite" and now try checking for the redirect endpoint to place our url** <br>
**-> There is a option beside of check stock named "next product"..** <br>
<img width="1166" height="472" alt="image" src="https://github.com/user-attachments/assets/ea6fc15e-e45f-47fd-a57f-d045e490b704" /><br>
**-> If we inspect that in burpsuite and found the endpoint as ```/product/nextproduct?path=http://url** <br>
**-> Now try it with the given url and it return "200 Ok" now try deleting the user ```carlos``` where path is ```/product/nextproduct?path=http://192.168.0.12:8080/admin/delete?username=carlos```** <br>
**-> The user got deleted and the lab is solved✅** <br><br>
















