# Prerequisites
* NodeJS >= 6
* NPM or Yarn

This version has been tested with Node `v8.1.2` and NPM `4.6.1` as well as NPM `5.3.0`.

# Installation

* **Opt #1. Download ZIP**

Not familiar with Git? Download the Full Version of the theme.
Extract the contents of ZIP file after downloading.
Downloading ZIP file does not help you to sync with further updates of the App.

* **Opt #2. Clone using GitStrap Web Client**

To setup the Full Version for the App on your system, with gitstrap tools to sync your app with constant updates, clone the repo.

* Install packages for Full Version

```bash
cd App
npm install
or
yarn
```

* **Firebase Backend only**: Run the following command `yarn generate`

* **To simulate for iOS**
    * Method One:
        * Run `npm start` in your terminal.
        * Scan the QR code in your Expo App.
    * Method Two:
        * Type npm run ios in your terminal.
* **To simulate for Android**
    * Method One:
        * Run `npm start` in your terminal.
        * Scan the QR code in your Expo App.
    * Method Two:
        * Make sure you have an Android emulator installed and running.
        * Type npm `run android` in your terminal.
        
## Seed Project

Once you are ready to use this template for your own project, you might want to remove some screens.
The entry point of the app is `App.js`, this file contains all the screens of the app organized into navigation routes.
Once you removed the unnecessary routes, you can remove the folder that correspond to the screens you would like to remove.
For instance, if you would like to remove the Overview screen, you need to remove its references from `App.js` and remove the `src/overview` folder.
It's that simple.
