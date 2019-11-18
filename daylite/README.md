# Files for Daylite CUCM Integration

## Overview
This folder contains 4 example files to answer questions posed to IGNW by the customer.

- `jabber-call-state.html` Shows how javascript in a Custom Tab can be used to provide call state to the jabber client
- `jabber-click-to-dial.html` An example of SIP and TEL URL's for testing click to dial from web pages.  This works with Firefox, but Chrome has a pop up each time
- `jabber-config.xml` An example of the config file that can be loaded into the CUCM for the Jabber clients to read on launch.  This will configure the clients with the custom tab needed to use the features in the html files
- `jabber-open-new-url.html` An example of how call detail passed to jabber can be used to open URL's to or perform other actions.

<hr>

## Using the files in the Jabber Client.
Download the repo to an http server.  From your local web browser, make sure you can navigate to the URL of the file.

- In Jabber for Mac or Windows, select File -> New Custom Tab...
- In the `Name` field, give the Custom Tab a name
- In the `Page URL` field, provide the URL to the file.
- Click OK to create a new custom tab

<hr>

## Jabber Call State
This file shows all the call state fields that are available to work with when an inbound call to the Jabber client happens.

This file must be loaded into Jabber as a Custom Tab in order to function.

<hr>

## Jabber Open New URL
This file shows how to work with a the inbound calling data to then search google.com for the inbound number

This file must be loaded into Jabber as a Custom Tab in order to function.

<hr>

## Jabber Click to Dial
This file provides some URL's to show the difference between tel:// and sip:// dialing.  You must open the page in a web browser then click on the links.

This file does not need to be loaded as a Custom Tab to operate.

NOTE: This works as desired in Firefox.  The first time you click, you can select Jabber as the preferred method of using the SIP URI then there after it will launch Jabber to make the calls.  With Chrome, Google disabled the remembering feature in v77 of Chrome.

https://support.google.com/chrome/thread/14194567?hl=en

<hr>

## Jabber Config File
The `jabber-config.xml` file is loaded into the root of all the CUCM TFTP servers.  In that file, all the Custom Tabs that need to be deployed can be defined and each Jabber client will download the file the next time it launches.


## Useful Links
### Jabber Parameters Reference (options for the jabber-config.xml file)
https://www.cisco.com/c/en/us/td/docs/voice_ip_comm/jabber/12_7/cjab_b_parameter-reference-guide-jabber-127.html
- `Jabber Client Configuration` chapter has info the structure of the file
- `Client` chapter has information the `jabber-plugin-config` parameter for the xml file
- `Options` chapter has details on further customizations of the tabs


### Specific Chapter for writing Custom Tab Javascript in the Feature and Options for Cisco Jabber Guide
https://www.cisco.com/c/en/us/td/docs/voice_ip_comm/jabber/12_7/cjab_b_feature-configuration-for-jabber-127/cjab_b_feature-configuration-for-jabber-127_chapter_0101.html?bookSearch=true

<hr>