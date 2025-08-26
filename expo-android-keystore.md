# Building Expo Android with Keystore

Building an Expo Android app with a keystore allows you to sign your APK or AAB for release on the Google Play Store.

## Prerequisites
- [Expo CLI](https://docs.expo.dev/get-started/installation/)
- [Node.js](https://nodejs.org/)
- An Expo project
- A keystore file (`.jks`)

## Steps

### 1. Generate a Keystore (if you don't have one)
```bash
keytool -genkeypair -v -keystore my-release-key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias my-key-alias
```

> **Note:** `keytool` comes with the Java JDK. [More info](https://developer.android.com/studio/publish/app-signing#generate-key)

### 2. Configure Expo to Use the Keystore

```bash
expo credentials:manager -p android
```
- Select `Update upload Keystore` and follow the prompts.

### 3. Build the Android App

```bash
expo build:android -t apk
# or for AAB
expo build:android -t app-bundle
```

### 4. Download the Build
Expo will provide a link to download your APK/AAB.

---

![Expo Android Build](https://docs.expo.dev/static/images/android-build.2e6e6e2b.png)

## References
- [Expo Android Build Docs](https://docs.expo.dev/classic/building-standalone-apps/#android)
