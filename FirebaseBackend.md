# Firebase Backend

There is an option of the theme available with a Firebase integration.
In this guide, we aim to guide you in setting up the app under your own firebase account and updating the backend of the app.

## Using your own Firebase account

To use your own Firebase account for this account, please create a new project and enable email/password authentication.
<img src="images/firebase/enable-email-notifications.png" width="300" style="margin: 16px;" />

From there you can go to `settings -> Add Firebase to your web app` and copy the given code snippet in `src/Firebase.js`.
This is how the beginning of the file looks like:

```js
import * as firebase from "firebase";

import {User} from "../Model";
import {DEFAULT_USER} from "../Constants";

const config = {
    apiKey: "...",
    authDomain: "...",
    databaseURL: "...",
    projectId: "...",
    storageBucket: "",
    messagingSenderId: "..."
};
```

Last step, you need to deploy the database validation and security rules to your account.
To generate the `rules.json` file run the following command:

```bash
yarn generate
```

`rules.json` is generated from `rules.bolt`.
Now you can login with the firebase cli using the command below:

```bash
firebase login
```

In `.firebaserc` you can replace the project id `react-native-do` with your own project id.
You are now ready to deploy the database rules using the following command:

```bash
yarn deploy
```

Et voilà! You are up and running with your own Firebase backend.

## Updating the backend

Of course, the data model of your app is likely to be quite different from the one we provided you with.
We use a single source of truth for the data model of the app which is contained in `rules.bolt`.
This file is written using the [Firebase Bolt Security and Modeling Language](https://github.com/firebase/bolt/blob/master/docs/language.md).
We use this file to generate the database security and validations rules (`rules.json`) but also the flow types for the React Native app (`src/Model.js`).

When modifying `rules.bolt`, you can re-generate the necessary artifacts using the following command:

```bash
yarn generate
```

And to deploy the new database rules:

```bash
yarn deploy
```

### Example

Assume you want to had a new property in the type `Profile` named `pictureURL`.
You can update the type definition the following way:

```bolt
type Profile {
    name: String,
    birthday: Number,
    pictureURL: String,
    emailNotifications: Boolean,
    phoneNotifications: Boolean
}
```

To re-generate the artifacts:

```bash
yarn generate
```

Now the code of the app needs to be refactored accordingly.
Flow type checker will point out these places for you.
Run: 

```bash
yarn flow
=>
src/Model.js:8
  8:   profile: Profile,
                ^^^^^^^ property `pictureURL` of Profile. Property not found in
  5:     profile : {
                   ^ object literal. See: src/Constants.js:5

```

Once the code refactoring is done, you can deploy the new database rules:

```bash
yarn deploy
```