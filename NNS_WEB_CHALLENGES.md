## WEB HACKER 2
**By exploring the given URL, we can navigate from page 1 to page 2 by modifying the page parameter directly in the URL. This indicates that the application allows direct manipulation of the object/page reference.** <br>
## Goal:
**To retrieve the flag, we need to take this attack a step further and it is said that "The admin user may have something interesting waiting for you"** <br>
## Soln:
<img width="497" height="681" alt="image" src="https://github.com/user-attachments/assets/9f7e6503-f0cc-41b0-824c-09e80b7561d9" /><br>
**-> A boarding-pass of user john is being displayed with all the details of gate number, seat number, group and all...** <br>
**-> Initially as they said of IDOR so let's try changing the passenger name or seat number or group etc.. (i.e, https://...../boarding-pass?group=2orpassenger=admin)** <br>
**-> But that all doesn't work and as they mentioned earlier that we need a tool that helps us to achieve some useful information.. For that let's take "burpsuite" which helps us in request and responses of it** <br>
**-> gone through the page source and found an API endpoint/path which is typically an HTTP GET request (Fetch API request)** <br>
<img width="765" height="182" alt="image" src="https://github.com/user-attachments/assets/f2712b86-04d3-46a8-bf58-f58f4a71f412" /><br>
**-> Go to burp and paste this boarding-pass request there and then send it to repeater after turning on the proxy** <br>
<img width="1565" height="736" alt="image" src="https://github.com/user-attachments/assets/caec6c4f-bf4f-4c70-9cb2-0b129f99acdd" /><br>
**-> So we observe that the path is just "/boarding-pass" after pasting the request, but from the page source it is observed that "/api/boarding-pass/<username>" so now try with the path mentioned in the page source but do no directly enter it in the burp, paste the total request with the path updated and then turn on proxy and check with john initially** <br>
<img width="1557" height="627" alt="image" src="https://github.com/user-attachments/assets/3abac08c-fb6d-4d20-9dd1-01568fd06ea5" /><br>
**-> The response is 200 ok so no try with the admin as username** <br>
<img width="1567" height="617" alt="image" src="https://github.com/user-attachments/assets/ef096c5d-4660-4db5-99c1-2f9166d70e07" /><br>
**-> The response for admin is also 200 ok now paste the qr barcode in a new tab and scan it and get the flag and paste it at the start...** <br><br>
<img width="1726" height="682" alt="image" src="https://github.com/user-attachments/assets/723be793-4ea2-45b7-9935-2a2503f42859" /><br>
## Got the Flag 🔥 













