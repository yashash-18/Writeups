# Stream
## Nmap Scan
<img width="825" height="491" alt="image" src="https://github.com/user-attachments/assets/2e02e9a4-1d2c-41f7-b4f7-200abb0b16a8" /><br>
**-> Found few open ports** <br>
**-> After visiting the http we found a message that "All terminal gateway systems are operational"** <br>
<img width="622" height="326" alt="image" src="https://github.com/user-attachments/assets/e031c6bc-91a1-4091-a0d9-a8ca5ba0c513" /><br>
**-> After visiting the ```port 8081```** <br>
<img width="636" height="322" alt="image" src="https://github.com/user-attachments/assets/653a941c-ed1c-4df7-ae86-69723755f316" /><br>
**-> So i checked for any endpoints by running the dirsearch, for ```port 80``` but couldn't get one** <br>
**-> Tried dirsearch for ```port 8081``` and found few paths** <br>
<img width="1422" height="361" alt="image" src="https://github.com/user-attachments/assets/68f22fdd-9a01-4cd0-a0be-df856f6fc236" /><br>
**-> Explored the ```/docs``` path** <br>
<img width="1467" height="447" alt="image" src="https://github.com/user-attachments/assets/260bcd20-8d5a-4ce2-9c34-1624726d884b" /><br>
**-> Inside the ```POST /feed/aidx``` there is an option to execute and it gives us the expected response** <br>
<img width="1437" height="676" alt="image" src="https://github.com/user-attachments/assets/f7a2ea22-49db-42b4-9588-392635954d5c" /><br>
**-> Also after checking that response try checking for AIDX flight-leg ingest and found that " It is an automated backend system that receives and processes real-time airline data formatted using the global IATA Aviation Information Data Exchange (AIDX) standard "** <br>

<div style="border: 1px solid #888; padding: 15px; border-radius: 8px;">
  
### AIDX (Aviation Information Data Exchange)
**-> The global, standardized "XML" data format used by airlines, airports, and flight status systems (like SITA or FlightAware) to share flight updates globally** <br>
**-> Instead of every airline using its own custom message format, they all format their data according to strict IATA definitions** <br>
-> Where **XML (eXtensible Markup Language) file is a plain-text file used to store and structure data in a format** that both humans and computers can easily read
</div><br>

**-> It says that "If an application parses an XML file with external entities enabled" it means that the website or software processing your XML file has a specific setting turned ON that allows the file to fetch data from the outside world.** <br>
**-> As per the given response and try sending a request by mention the xml file** <br>
```
 curl -X 'POST' \
  'http://api.htb-airport.htb:8081/feeds/aidx' \
  -H 'accept: */*' \
  -d '<?xml version="1.0" encoding="UTF-8"?>
<IATA_AIDX_FlightLegNotifRQ 
    xmlns="http://iata.org" 
    xmlns:xsi="http://w3.org" 
    TargetStructure="FlightLeg" 
    Version="1.0">
    <Originator>
        <AirlineCode>AI</AirlineCode>
    </Originator>
    <FlightLeg>
        <LegIdentifier>
            <AirlineIATA>AI</AirlineIATA>
            <FlightNumber>101</FlightNumber>
            <OriginAirport>BOM</OriginAirport>
            <DestinationAirport>LHR</DestinationAirport>
            <ScheduledDepartureDate>2026-10-14</ScheduledDepartureDate>
        </LegIdentifier>
    </FlightLeg>
</IATA_AIDX_FlightLegNotifRQ>'
```
**-> Got the response as** <br>
<img width="592" height="336" alt="image" src="https://github.com/user-attachments/assets/47b5a1c1-1f95-4d32-9eb3-13d14095a8f6" /><br>
**-> 









