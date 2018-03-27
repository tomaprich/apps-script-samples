<<<<<<< HEAD
# Google Apps Script Samples

Various sample code and projects for the Google Apps Script platform. Learn more at
[https://developers.google.com/apps-script](https://developers.google.com/apps-script).

* Advanced: Apps Script's advanced services
* Android: Android add-ons
* Calendar: Create a vacation calendar
* Docs: Cursor inspector and translate add-ons
* Gmail: Sending mail and mailmerge
* Forms: Forms notification add-on
* Sheets: Sheets add-ons and custom functions
* Slides: Sidebar and translate add-ons

## Clone using the `clasp` command line tool

Learn how to clone, pull, and push Apps Script projects on the command line
using [clasp](https://developers.google.com/apps-script/guides/clasp).
=======
# Dialog to Sidebar Communication in Apps Script

This script demonstrates a method of setting up a communication channel between
a dialog and a sidebar in Apps Script. This helps solve the common problem
of having your sidebar know when a dialog is opened, is submitted, closed, etc.

With the introduction of the IFRAME sandbox mode, HtmlService UIs can take
advantage of the
[HTML5 localStorage API](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage).
The open source library [intercom.js](https://github.com/diy/intercom.js/)
builds a messaging system on top of this API, allowing for dialogs and sidebars
in the same browser to communicate with each other.

An overview of the process is as follows:

* The sidebar requests a new dialog to be opened.
* The backend generates a new ID for the dialog, opens the dialog (passing in
  that ID as a template parameter), and sends the ID back to the sidebar.
* The sidebar listens for events on the dialog's intercom.js channel.
* The dialog regularly "checks in" with the sidebar, resetting a
  [timer](https://developer.mozilla.org/en-US/Add-ons/Code_snippets/Timers).
* When the user completes the dialog (by clicking either the "OK" or "Cancel"
  button) it sends this status change to the sidebar.
* If the sidebar's timer actually fires, that means the dialog hasn't checked in
  recently, and it is considered "lost".
>>>>>>> af25ecfdf4549e99795f3e867c9b890024bba66c
