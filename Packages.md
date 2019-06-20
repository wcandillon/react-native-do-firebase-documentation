# Packages Used

```json
{
    "name": "react-native-do-firebase",
    "version": "1.2.6",
    "private": true,
    "devDependencies": {
        "babel-eslint": "^8.2.1",
        "babel-preset-expo": "^5.0.0",
        "eslint": "^4.9.0",
        "eslint-config-airbnb": "^16.1.0",
        "eslint-plugin-flowtype": "^2.41.0",
        "eslint-plugin-import": "^2.7.0",
        "eslint-plugin-jsx-a11y": "^6.0.2",
        "eslint-plugin-react": "^7.4.0",
        "eslint-plugin-react-native": "^3.2.1",
        "expo-cli": "2.20.2",
        "firebase-bolt": "0.8.2",
        "firebase-bolt-transpiler": "git+https://github.com/wcandillon/firebase-bolt-transpiler#e4172ab14a43a3dd6f29711582a9780d91e93238",
        "firebase-tools": "7.0.0",
        "flow-bin": "0.63.1",
        "flow-result-checker": "^0.3.0",
        "jest-expo": "^33.0.0",
        "react-test-renderer": "16.0.0-alpha.12"
    },
    "main": "node_modules/expo/AppEntry.js",
    "scripts": {
        "generate": "firebase-bolt < rules.bolt > rules.json && firebase-bolt-transpiler --flow < rules.bolt > src/Model.js",
        "deploy": "firebase deploy",
        "start": "expo start",
        "eject": "expo eject",
        "android": "expo android",
        "ios": "expo ios",
        "test": "jest",
        "test:watch": "jest --watch",
        "flow": "flow check --show-all-errors | flow-result-checker",
        "lint": "eslint App.js App.test.js src/",
        "install": "firebase-bolt < rules.bolt > rules.json && firebase-bolt-transpiler --flow < rules.bolt > src/Model.js"
    },
    "jest": {
        "preset": "jest-expo"
    },
    "dependencies": {
        "@expo/vector-icons": "6.3.1",
        "autobind-decorator": "1.4.0",
        "colors": "1.0.3",
        "expo": "^33.0.0",
        "firebase": "5.8.0",
        "jest-junit-reporter": "1.1.0",
        "lodash": "4.17.4",
        "mobx": "3.1.9",
        "mobx-react": "4.1.8",
        "moment": "2.18.1",
        "native-base": "2.12.1",
        "react": "16.8.3",
        "react-native": "https://github.com/expo/react-native/archive/sdk-33.0.0.tar.gz",
        "react-native-card-carousel": "git+https://github.com/wcandillon/react-native-card-carousel#6dc8048",
        "react-native-datepicker": "1.6.0",
        "react-navigation": "^3.11.0",
        "throttle-debounce": "1.0.1"
    }
}
```
