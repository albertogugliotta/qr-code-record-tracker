# QR-Code-Record-Tracker
**Salesforce Record Tracker:** Keep track of your Asset by relating a record to it and stick the generated QR Code on it. 
- Its a simple fomula that works independently to the Salesforce edition used.
- Easily retrieve the information related to the Asset through the SF1 App.
- Feel free to use any Code Scanner App in the market to scan the QR Code, then open the result with SF1.

**Formula:**

IMAGE('http://api.qrserver.com/v1/create-qr-code/?data='& (LEFT($Api.Enterprise_Server_URL_210, FIND( "/services", $Api.Enterprise_Server_URL_210) -1)&'/'&Id) &'&size='&TEXT(QR_Code_Size__c),"")

<img src="https://cloud.githubusercontent.com/assets/4924744/16903329/ba8e54e6-4c51-11e6-8548-79edd067b79b.png" width="600">
