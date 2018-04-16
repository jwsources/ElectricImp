# Electric Imp
Device and Agent code to use the Electric Imp developer device with Salesfore Platform Events.
Added accelerometer sensor Library and absolute pressure sensor Library.

Code is based on the Salesforce Trailhead project 'Build an IoT Integration with Electric Imp', https://trailhead.salesforce.com/projects/workshop-electric-imp.

If you see the message  "Session expired or invalid", "errorCode": "INVALID_SESSION_ID" in your console in the Electric Imp IDE when starting your Electric Imp it means you need to reautheticate against the Salesforce Org you've setup. This is as simple as clicking on the agent url shown in the IDE.

Make sure the Agent Code is using your Consumer Key and Consumer Secret, variables are at the bottom!

I also didn't follow the naming scheme from the Trailhead project, so my Platform event:
API Name: Electric_Imp_Reading__e, you can use your own with the variable in the Agent Code at the same location where you have to enter your Consumer Key and Consumer Secret.

This also means I added the new reading enabled for pressure and the accelerometer to Salesforce, these are the custom fields on my Electric_Imp_Reading Platform Event:
AccelX__c	Number(4, 4),
AccelY__c	Number(4, 4),
AccelZ__c	Number(4, 4),
DeviceID__c	Text(16),
Humidity__c	Number(4, 2),
Light__c	Text(10),
Pressure__c	Number(6, 2),
Temperature__c	Number(4, 2),
Timestamp__c	Date/Time

The content data currently looks like
{ "DeviceID__c": "23710f24c448e0ee", "Pressure__c": 1017.21, "AccelX__c": 0.508, "AccelZ__c": -0.872, "Humidity__c": 37.6896, "Temperature__c": 20.54, "AccelY__c": 0.148, "Light__c": "Off", "Timestamp__c": "2018-03-19T09:54:29Z" }.

Temperature is taken from the pressure sensor, can be changed.

To add the new data to a record in Salesforce, modify the Object to add new fields and change the Apex trigger on the Platform Event.

