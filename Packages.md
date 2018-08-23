# Packages Used

```json
{
    "name": "react-native-do-firebase",
    "version": "1.2.4",
    "private": true,
    "devDependencies": {
        "babel-eslint": "^8.2.1",
        "eslint": "^4.9.0",
        "eslint-config-airbnb": "^16.1.0",
        "eslint-plugin-flowtype": "^2.41.0",
        "eslint-plugin-import": "^2.7.0",
        "eslint-plugin-jsx-a11y": "^6.0.2",
        "eslint-plugin-react": "^7.4.0",
        "eslint-plugin-react-native": "^3.2.1",
        "exp": "55.0.5",
        "expo-cli": "^1.1.0-beta.4",
        "firebase-bolt": "0.8.2",
        "firebase-bolt-transpiler": "git+https://github.com/wcandillon/firebase-bolt-transpiler#e4172ab14a43a3dd6f29711582a9780d91e93238",
        "firebase-tools": "3.9.2",
        "flow-bin": "0.63.1",
        "flow-result-checker": "^0.3.0",
        "jest-expo": "^29.0.0",
        "react-native-scripts": "1.11.1",
        "react-test-renderer": "16.0.0-alpha.12"
    },
    "main": "./node_modules/react-native-scripts/build/bin/crna-entry.js",
    "scripts": {
        "generate": "firebase-bolt < rules.bolt > rules.json && firebase-bolt-transpiler --flow < rules.bolt > src/Model.js",
        "deploy": "firebase deploy",
        "start": "expo-cli start",
        "eject": "react-native-scripts eject",
        "android": "react-native-scripts android",
        "ios": "react-native-scripts ios",
        "test": "node node_modules/jest/bin/jest.js",
        "test:watch": "node node_modules/jest/bin/jest.js --watch",
        "flow": "flow check --show-all-errors | flow-result-checker",
        "lint": "eslint App.js App.test.js src/",
        "install": "firebase-bolt < rules.bolt > rules.json && firebase-bolt-transpiler --flow < rules.bolt > src/Model.js"
    },
    "jest": {
        "preset": "jest-expo",
        "transformIgnorePatterns": [
            "node_modules/(?!react-native|react-navigation|expo|native-base-shoutem-theme|@shoutem|react-clone-referenced-element|native-base|@expo|mobx-react)"
        ],
        "testResultsProcessor": "./node_modules/jest-junit-reporter"
    },
    "dependencies": {
        "@expo/vector-icons": "6.3.1",
        "autobind-decorator": "1.4.0",
        "colors": "1.0.3",
        "expo": "^29.0.0",
        "firebase": "4.12.1",
        "jest-junit-reporter": "1.1.0",
        "lodash": "4.17.4",
        "mobx": "3.1.9",
        "mobx-react": "4.1.8",
        "moment": "2.18.1",
        "native-base": "2.4.1",
        "react": "16.3.1",
        "react-native": "https://github.com/expo/react-native/archive/sdk-29.0.0.tar.gz",
        "react-native-card-carousel": "git+https://github.com/wcandillon/react-native-card-carousel#6dc8048",
        "react-native-datepicker": "1.6.0",
        "react-navigation": "^2.9.3",
        "throttle-debounce": "1.0.1"
    }
}
```
