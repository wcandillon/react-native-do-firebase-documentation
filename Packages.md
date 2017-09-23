# Packages Used
 
```json
{
    "name": "react-native-do-backend",
    "version": "1.0.0",
    "private": true,
    "devDependencies": {
        "autobind-decorator": "1.4.0",
        "babel-eslint": "7.2.3",
        "eslint": "3.19.0",
        "eslint-config-google": "0.7.1",
        "eslint-plugin-flowtype": "2.32.1",
        "eslint-plugin-react": "6.10.3",
        "exp": "40.0.2",
        "firebase-bolt": "0.8.2",
        "firebase-bolt-transpiler": "git+https://github.com/wcandillon/firebase-bolt-transpiler#e4172ab14a43a3dd6f29711582a9780d91e93238",
        "firebase-tools": "3.9.2",
        "flow-bin": "^0.49.1",
        "react-native-scripts": "1.3.1",
        "jest-expo": "~20.0.0",
        "react-test-renderer": "16.0.0-alpha.12"
    },
    "main": "./node_modules/react-native-scripts/build/bin/crna-entry.js",
    "scripts": {
        "generate": "firebase-bolt < rules.bolt > rules.json && firebase-bolt-transpiler --flow < rules.bolt > src/Model.js",
        "deploy": "firebase deploy",
        "start": "react-native-scripts start",
        "eject": "react-native-scripts eject",
        "android": "react-native-scripts android",
        "ios": "react-native-scripts ios",
        "test": "node node_modules/jest/bin/jest.js",
        "test:watch": "node node_modules/jest/bin/jest.js --watch",
        "flow": "flow",
        "lint": "eslint App.js App.test.js src/",
        "install": "firebase-bolt < rules.bolt > rules.json && firebase-bolt-transpiler --flow < rules.bolt > src/Model.js"
    },
    "jest": {
        "preset": "jest-expo",
        "transformIgnorePatterns": [
            "node_modules/(?!react-native|react-navigation|expo|native-base-shoutem-theme|@shoutem|react-clone-referenced-element)"
        ],
        "testResultsProcessor": "./node_modules/jest-junit-reporter"
    },
    "dependencies": {
        "@expo/vector-icons": "5.2.0",
        "firebase": "4.2.0",
        "jest-junit-reporter": "1.1.0",
        "lodash": "4.17.4",
        "mobx": "3.1.9",
        "mobx-react": "4.1.8",
        "moment": "2.18.1",
        "native-base": "2.3.1",
        "expo": "^20.0.2",
        "react": "16.0.0-alpha.12",
        "react-native": "^0.47.0",
        "react-native-card-carousel": "git+https://github.com/wcandillon/react-native-card-carousel#6dc8048",
        "react-native-datepicker": "1.6.0",
        "react-navigation": "1.0.0-beta.11",
        "throttle-debounce": "1.0.1"
    }
}
```
