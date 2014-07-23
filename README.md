Jira Notifications Chrome Extension
===================================

This chrome extension will allow you to show jira notifications on your toolbar or desktop.

Requirements
------------

* Google Chrome Version 23 or higher
* Jira rest api must be enabled

Regarding Security
------------------

One thing you will notice if you view the permissions for this extension is that it can
* Access your data on all websites
* Access your tabs and browsing activity

This sounds alarming which is understandable, but the extension does not collect data. These permissions are due to our need to access _any_ instance of jira that you specify.

In terms of the options specified, these are local to your machine only. The only thing to be aware of is that your username and password are sent in an authorization header base64 encoded.

Installation
------------

Below are the directions for installation:
* Download jinotify.crx from this page
* Open the folder containing jinotify.crx
* In chrome, go to the url chrome://extensions
* Drag jinotify.crx from the folder into the chrome://extensions page
* Once installed, launch the options page which you can find under the jinotify plugin section on the extensions page
* In the options page you will need to specify the server, username, password, and frequency of which to grab updates
* After saving the options you should start seeing notifications 1 minute later (assuming there have been updates within your frequency period)

In regards to the frequency setting, this number is how often the extension will call the jira for updates.
Example:
If your frequency is set to 10 minutes and the time is currently 9:50AM, jira will be called at 9:50AM and request data for the past 10 minutes (9:40AM - 9:50AM). Once data is collect it will then run again at 10:00AM and so on.

Future Features
---------------

* Better handling of time returns (eg: display as 5m ago)
* Select which notifications to see
* -Bulking of notifications-
