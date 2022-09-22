# React Native Web With Typescript

This is a basic template that setups React Native with typescript and web support using webpack.

In order to use this template, you need to follow the [React Native setup guide](https://reactnative.dev/docs/environment-setup) first.

After that, you should run `npm install`.

### Rename the project

After installing all dependencies, you should run `npx react-native-rename <name_of_you_project> -b <name_of_package>` to change the project name from "reactNativeWebTypescriptTemplate" to whatever you like. For example:

`npx react-native-rename myProject -b com.myOrganizationName.myProyect`

## Development with hot reload

To run in development mode on Android or IOS run `npm run start`.
And in another terminal one of the following:

- `npm run ios`
- `npm run android`

To run in development mode on Web just run `npm run web`.

## Production Build

### Android

Before building for android, run `npm run generate-android-signature` to generate the keys to signe your app. This is needed to upload the app bundle to the app store.

Then open `android/app/gradle.properties`, update it with the password you setted in the previous step and add the file to `.gitignore`. This info should not be on your repo!

After setting up the gradle properties, run `npm run build:android` to generate the bundle. It will be saved on `android/app/build/outputs/bundle/release`

To install the bundled app on a connected device or a simulator run `npm run install:android`.

Once tested, you can upload the bundle to [Google Play Console](https://play.google.com/console).

Take in consideration that the generated bundle has obfuscated code, you should also upload `android/app/build/outputs/mapping/release/mapping.txt`. This will allow you see the original strack trace for user-reported issues in the Play Console.

### WEB

In order to build for web just run `npm run build:web`. The compiled applicatión site will be stored in `dist` folder.
