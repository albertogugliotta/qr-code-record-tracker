# QR-Code-Record-Tracker for Salesforce 
Keep track of your Asset by relating a record to it and stick the generated QR Code on it. 
- Its a simple fomula that works independently to the Salesforce edition used.
- Easily retrieve the information related to the Asset through the SF1 App.
- Feel free to use any Code Scanner App in the market to scan the QR Code, then open the result with SF1.

##**Formula**

```
IMAGE('http://api.qrserver.com/v1/create-qr-code/?data='& (LEFT($Api.Enterprise_Server_URL_210, FIND( "/services", $Api.Enterprise_Server_URL_210) -1)&'/'&Id) &'&size='&TEXT(QR_Code_Size__c),"")
```

**_QR_Code_Size__c_** _is a picklist which defines the size of the Code. e.g. 50x50, 70x70, 100x100_

##**Result**

<img width="210" alt="qrcode-example" src="https://cloud.githubusercontent.com/assets/4924744/22618912/e162493e-eacf-11e6-8093-aec643e54de4.png">
