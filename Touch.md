# Touch
### Nmap Scan
<img width="552" height="171" alt="image" src="https://github.com/user-attachments/assets/375a57e9-5b5f-4e48-8734-85ca699f80af" /><br>
**-> Found few open ports and services running.** <br>
**-> After many attempts of approaching then tried endpoint enumeration using ```ffuf```** <br>
**-> Run ```ffuf -u https://touch.htb:8443/FUZZ -w /usr/share/seclists/Discovery/Web-Content/raft-small-words.txt -k```** <br>
**-> After the run we will get many endpoints now check for the status other than 302 and found an endpoint ```/api``` and agin using this try again to find one more end point and then found ```/api/status/```** <br>
**-> After that by sending the curl request found the serial number which acts as the password to the Nexion Docreader** <br>
```
curl -i http://10.129.147.139:8443/api/status

HTTP/1.1 200 OK
Transfer-Encoding: chunked
Content-Type: application/json
Server: Microsoft-HTTPAPI/2.0
Access-Control-Allow-Origin: *
Access-Control-Allow-Methods: GET, POST, PUT, OPTIONS
Access-Control-Allow-Headers: Content-Type
Date: Wed, 07 Oct 2026 23:44:38 GMT

{"device":"Nexion DeviceHub DH-100","serial":"NX-DH-2024-B7042","firmware":"1.4.2","status":"online","uptime":85478}%
```
**-> After login found the creds of a user and there are few features like scanner, printer, and also there's an upload option**
<img width="1910" height="532" alt="image" src="https://github.com/user-attachments/assets/870e11e2-5129-4130-bdce-4b321c0bfb0b" /><br>
**-> With those creds try to log in to RDP, and found Successfully logged into RDP** <br>
<img width="1857" height="796" alt="image" src="https://github.com/user-attachments/assets/8ac904a7-e842-496a-88eb-98b36babbd23" /><br>
**-> After exploring everything lets turn of the scanner and printer** <br>
**-> After connecting to RDP at the right corner there is a option named ```staff login``` after clicking it there is an option to scan badge then it displays as troubleshooting error and now try to view the troubleshooting to check for the error** <br>
<img width="767" height="432" alt="image" src="https://github.com/user-attachments/assets/71a0eb06-3669-4482-b22d-70f318757552" /><br>
**-> Click on it and then a web browser is being displayed with troubleshoot error and after trying multiple ways and found to connect to command prompt..** <br>
<img width="1457" height="812" alt="image" src="https://github.com/user-attachments/assets/f73ae76a-2948-454b-ad9b-a11728d1f69f" /><br>
**-> Run ```file:///C:/windows/system32/cmd.exe``` and immediately it is being displayed that it is downloaded and then if we try to view that in folders then in desktop there is a file named ```user```, and found that it contains user flag..** <br>
<img width="1112" height="532" alt="image" src="https://github.com/user-attachments/assets/58223de1-70cb-42d3-bb7b-464cdbcbdf5a" /><br>








