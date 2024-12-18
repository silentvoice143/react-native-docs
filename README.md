# Resources

## For styling
- tailwind css
  Some packages:
  - [https://www.npmjs.com/package/twrnc](https://www.npmjs.com/package/twrnc)
  - [https://www.npmjs.com/package/nativewind](https://www.npmjs.com/package/nativewind)

## Components

- [React Native Paper](https://callstack.github.io/react-native-paper/docs/guides/getting-started)
- [React Native Elements](https://reactnativeelements.com/docs)
- [UI kitten](https://akveo.github.io/react-native-ui-kitten/docs/getting-started/what-is-ui-kitten#what-is-ui-kitten)
- [RNUILib](https://wix.github.io/react-native-ui-lib/)
- [Shoutem UI](https://shoutem.github.io/docs/ui-toolkit/components)
- [gluestack UI](https://gluestack.io/)

## Animation Library
- [Reanimated](https://docs.swmansion.com/react-native-reanimated/)
- [React native animatable](https://github.com/oblador/react-native-animatable)
- [React native motion](https://github.com/xotahal/react-native-motion)
- [Lottie](https://airbnb.io/lottie/#/)-[LottieFiles](https://lottiefiles.com/)for free animation

## Build .apk and .abb file

- [video](https://www.youtube.com/watch?v=M0fX3VpIiN8)
- [doc](https://reactnative.dev/docs/signed-apk-android)

## Update the version and build
1. Update versionCode and versionName in build.gradle:

- Open the android/app/build.gradle file.
- Locate the defaultConfig block and update the versionCode and versionName fields to your desired version.
```
defaultConfig {
    applicationId 'com.shakeapp.shakeapp'
    minSdkVersion rootProject.ext.minSdkVersion
    targetSdkVersion rootProject.ext.targetSdkVersion
    versionCode 16      // Increment this value
    versionName "1.6.0" // Update this value to your desired version
}

```

2. Open the package.json file in your project's root directory.
Update the version field to match the new version.

3. Open a terminal and navigate to the Android directory of your project:

```
cd android
```
Clean the project (optional but recommended to avoid potential build issues):

```
./gradlew clean
```
Build the release APK:

```
./gradlew assembleRelease
```
The generated .apk file will be located in android/app/build/outputs/apk/release/app-release.apk.

Build the release AAB (Android App Bundle):

```
./gradlew bundleRelease
```
The generated .aab file will be located in android/app/build/outputs/bundle/release/app-release.aab.
