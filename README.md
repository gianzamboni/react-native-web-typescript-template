# React Native Web With Typescript

===================================

This is a basic template that setups React Native with typescript and web support using webpack.

## Usage

===================================
In order to use this template, you need to follow the [React Native setup guide](https://reactnative.dev/docs/environment-setup) first.

After that, you should run `npm install`.

To run in development mode run `npm run start`.
And in another terminal one of the following:

- `npm run web`
- `npm run ios`
- `npm run android`

## Production Build

### Android

Before building for android, run `npm run generate-release-signature` to generate the keys to signe your app. This is needed to upload the app bundle to the app store.

Then open `android/app/gradle.properties` and update it with the password you setted in the previous step.

After setting up the gradle properties, run `npm run build:android` to generate the bundle. It will be saved on `android/app/build/outputs/bundle/release`

To install the bundled app on a connected device or a simulator run `npm run install:android`.

Once tested, you can upload the bundle to [Google Play Console](https://play.google.com/console).
