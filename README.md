# slack-status-based-on-wifi-name
Set your status on Slack based on the WiFi network you are connected to.

## How does it work?

The script checks periodically the WiFi network name (SSID) you are connected to and sets your status on Slack according to the mapping defined in [config.js](./config.js).
Screenshot example: ![Wifi based slack status change screenshot](https://raw.githubusercontent.com/Indivirtual/wifi-based-slack-status/master/docs/set-slack-status-based-on-wifi.png "Wifi based slack status change screenshot")

## How to run it?
Currently only works on Windows and macOS only

You need to obtain a Slack token for your account from https://api.slack.com/custom-integrations/legacy-tokens.
Copy and paste the token into [config.js] slackToken variable

You also need to have node.js installed to run the script. Currently it works on Windows and macOS only.
Install nodejs using this link: https://nodejs.org/en/download/
- Clone or download this repository
- Install dependencies with `npm install`
- Copy and paste the token into [config.js] slackToken variable
- Run with `npm start`

## Things to know

Be careful with defining a updateInterval value that is too low. Slack will block requests for status change if done too frequently.
Run this program as a service (in Windows) using NSSM (the Non Sucking Service Manager) at http://nssm.cc/
Check the Indivirtual blog for more information on how to do this: https://blog.indivirtual.nl/update-slack-status-automatically-using-node-js

## Shoutout
Thanks for Lukasz Wiktor for the initial code: https://github.com/LukaszWiktor/slack-status-based-on-wifi-name
Thanks Jaco Koster for the update!
