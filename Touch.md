# Touch
### Nmap Scan
<img width="552" height="171" alt="image" src="https://github.com/user-attachments/assets/375a57e9-5b5f-4e48-8734-85ca699f80af" /><br>
**-Found few open ports and services running.** <br>
**-After many attempts of approaching then tried endpoint enumeration using ```ffuf```** <br>
**-Run ```ffuf -u https://touch.htb:8443/FUZZ -w /usr/share/seclists/Discovery/Web-Content/raft-small-words.txt -k```** <br>
**-After the run we will get many endpoints now check for the status other than 302 and found an endpoint ```/api``` and agin using this try again to find one more end point and then found ```/api/status/```** <br>
**-After that by sending the curl request found the serial number which acts as the password to the Nexion Docreader** <br>
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

{"device":"Nexion DeviceHub DH-100","serial":"NX-DH-2024-B7042","firmware":"1.4.2","status":"online","uptime":85478}%  ```

