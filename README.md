# TermPage
[![Netlify Status](https://api.netlify.com/api/v1/badges/a42a6857-c585-4526-a58e-2338fa2bb519/deploy-status)](https://app.netlify.com/sites/cocky-fermat-c0aaaf/deploys)

A simple and minimal terminal style start page with [Dracula](https://draculatheme.com/) colors


Code borrowed from https://gitlab.com/madsouris/startpage. I just pimped it a bit up and changed the colors for my setup. 

![screenshot](screenshot.png)

Live preview [here](https://cocky-fermat-c0aaaf.netlify.app/)

## Installation

### Installation on Chrome

1. Clone this repository ```git clone https://github.com/Mofiqul/termpage.git```
2. Open extensions from the tool menu or open it from chrome://extensions
3. Click on Load unpacked, navigate to the directory where you cloned the repo and select it.

### Firefox Building & Signing
To make the termpage extension permanent and not have to re-add the extension every time you restart Firefox, you must build the extension/your config and get it signed by Mozilla.

#### Building the extension

Install node.js/npm from [nodejs.org](nodejs.org) so we can install the web-ext tools.

To install the web-ext tools so we can build the extension, run this command in a terminal after installing npm:

```npm install -g web-ext```

Then change directory into the same directory as the termpage extension files.
Example: ```cd termpage``` Then use web-ext to build the extension:

```web-ext build```

This will create a directory called web-ext-artifacts and in which there will be a zip file. This file is your built extension.

#### Signing the built extension

To get the extension signed by Mozilla you have to go to the [Mozilla Developer Hub](https://addons.mozilla.org/en-US/developers/) and sign in with a Firefox Account.

1. Click "Submit Your First Addon"
2. Select "Distribute on my own"
3. Then click "Upload File" and select the termpage directory, then web-ext-artifacts, then the zip file that was just created.
4. Then select compatibility with Firefox and Firefox for Android
5. Then hit "Sign add-on", Click "No" for source-code distribution and then wait 5-10 minutes.

#### Downloading the signed extension
Once you've waited 5-10 minutes your extension should have been signed.

To download the extension go to the Developer Hub and click the button that says "View All Submissions"

Then click "termpage"

Then on the left sidebar click "Manage Status & Versions"

**Tip: To update the extension change the extension's version number in manifest.json, build the extension, and then click "Upload a new version" on this page, then follow the steps below.**

Then in the top version number's section check the "Status" if it says "Approved" then you are good to go!

Then click the top version number

Then under files, click the .xpi file and install it!

> This instruction is taken from [here](https://github.com/deepjyoti30/startpage/wiki/How-to-sign-the-extension-for-Personal-Use-on-Firefox). 

#### Opening termpage on new tab

1. Go to this url in firefox: ```about:debugging#/runtime/this-firefox```
2.Find the extension and copy the manifest url
3. Go into the preferences and set the homepage as the manifest url but replace the end of the url with ```index.html``` instead of ```manifest.json```

> This instruction is taken from [here](https://github.com/deepjyoti30/startpage/wiki/Installation#opening-startpage-on-new-tab). 
