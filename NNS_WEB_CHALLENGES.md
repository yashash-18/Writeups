# WEB HACKER 2
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

# Simon
## GOAL:
**I am Simon. I need to select the optimal seat(best available seat) for the upcoming flight!!** <br>
## Condition:
**We need to unlock NNS Air plus seats as they deliver a superior travel experience designed around enhanced comfort, flags, flexibility, and convenience. Given: Upgrade your journey with premium benefits that make every kilometer work harder for you.** <br>
## Soln:
**-> By accessing the given URL, a webpage displaying available seats along with ‘Save’ option is displayed** <br>
<img width="525" height="752" alt="image" src="https://github.com/user-attachments/assets/01057aae-ba9b-4abb-9607-7fdf7c57866a" /><br>
**-> Explored the page source and found that flag obj is also present but it not allowed to display (display:none)** <br>
<img width="395" height="175" alt="image" src="https://github.com/user-attachments/assets/7bbd1ad4-4e3b-41e4-8e14-162453eb0459" /><br>
**-> where flag object contains the flag in FLAG** <br>
<img width="1066" height="160" alt="image" src="https://github.com/user-attachments/assets/39c96cc2-a4ee-4000-9c86-c223ce7600bd" /><br>
**->  Also an endpoint was found that uses the POST method when the user clicks save after selecting the seat, while the initial request made by the browser uses the GET method** <br>
<img width="537" height="337" alt="image" src="https://github.com/user-attachments/assets/db8496a7-db69-422c-ad50-4f6031def311" /><br>
**-> Now make a POST request with the "/save" as endpoint and also include the content-type and the selected seat number from the terminal** <br>
<img width="560" height="97" alt="image" src="https://github.com/user-attachments/assets/911d8fe3-46b5-43e4-baef-c5b60ac01e40" /><br>
**-> The response is true, so lets extract the details of it by including the verbose flag.** <br>
<img width="942" height="791" alt="image" src="https://github.com/user-attachments/assets/17e65e48-946a-442c-83f3-54ce8c91c9a2" /><br>
**-> Copy the URL and now we will see that the flag is being displyed saying that we booked the NNS Air plus seat** <br>
<img width="650" height="742" alt="image" src="https://github.com/user-attachments/assets/f15b8724-d42a-4733-bc84-da3206a56f58" /><br>
**Paste the flag at the start** <br>
<img width="1705" height="685" alt="image" src="https://github.com/user-attachments/assets/7a58e740-a223-4765-809a-6e3dc59a3972" /><br>
## Got the Flag 🔥 


























