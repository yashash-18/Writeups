# Touch
### Nmap Scan
<img width="552" height="171" alt="image" src="https://github.com/user-attachments/assets/375a57e9-5b5f-4e48-8734-85ca699f80af" /><br>
**-Found few open ports and services running.** <br>
**-After many attempts of approaching then tried endpoint enumeration using ```ffuf```** <br>
**-Run ```ffuf -u https://touch.htb:8443/FUZZ -w /usr/share/seclists/Discovery/Web-Content/raft-small-words.txt -k```** <br>
**-After the run we will get many endpoints now check for the status other than 302 and found an endpoint ```/api``` and agin using this try again to find one more end point and then found ```/api/status/```** <br>

