# Electric Imp
Device and Agent code to use the Electric Imp developer device with Salesfore Platform Events.
Added accelerometer sensor Library and absolute pressure sensor Library.

Code is based on the Salesforce Trailhead project 'Build an IoT Integration with Electric Imp', https://trailhead.salesforce.com/projects/workshop-electric-imp.

Make sure the Agent Code is using your Consumer Key and Consumer Secret!

I also didn't follow the naming scheme from the Trailhead project, so my Platform event:

API Name: Electric_Imp_Reading__e

Custum fields: DeviceID__c, Humidity__c, Light__c, Temperature__c, Timestamp__c, Pressure__C, AccelX__c, AccelY__c, AccelZ__c

This also means I added the new reading enabled for pressure and the accelerometer to Salesforce, the content data currently looks like
{ "DeviceID__c": "23710f24c448e0ee", "Pressure__c": 1017.21, "AccelX__c": 0.508, "AccelZ__c": -0.872, "Humidity__c": 37.6896, "Temperature__c": 20.54, "AccelY__c": 0.148, "Light__c": "Off", "Timestamp__c": "2018-03-19T09:54:29Z" }.

