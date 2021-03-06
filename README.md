## iCal Integration

ERPNext App for iCal Feed

### Introduction

This app lets you easily subscribe to an iCal feed originating from your frappe or ERPNext instance. Once set up you will be able to subscribe a calender in which all events marked as public are posted to. Like all iCal feeds this is just a one-way sync.

## Setup
### Server Side
For being able to use the app you will need to install a iCal library on your server. To install the iCal library you would
need to go to your frappe-bench directory and install iCalendar using ```./env/bin/pip install icalendar```

Once installed you need to open iCal Subscriptions DocType via the global search on your instance. There you can activate the functionality and set a secret which is needed to subscribe to the feed.

### Client Side
You can use most calendar apps to subscribe to an iCal feed. iCal feeds are often used in sports calanedars or holiday lists in your country.
Once you have setup Server Side you can reach your iCal feed with the following address

  https://myerpdomain.com/api/method/icalfeed.icalfeed.utils.calendar.download_calendar?secret=[secret]
  
myerpdomain.com is your ERPNext instances Domain and [secret] is the secret set in the DocType iCal Feed Settings.

Tested in Thunderbird an Apples Calendar.

#### License

GNU GPLv3
