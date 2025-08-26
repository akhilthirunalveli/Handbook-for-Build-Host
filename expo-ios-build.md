# Building Expo iOS App

Building an Expo iOS app for release requires an Apple Developer account and proper certificates.

## Prerequisites
- [Expo CLI](https://docs.expo.dev/get-started/installation/)
- [Node.js](https://nodejs.org/)
- An Expo project
- Apple Developer account

## Steps

### 1. Login to Expo
```bash
expo login
```

### 2. Start the iOS Build
```bash
expo build:ios
```
- Follow the prompts to let Expo handle credentials or provide your own.

### 3. Download the Build
Expo will provide a link to download your `.ipa` file.

---

![Expo iOS Build](https://docs.expo.dev/static/images/ios-build.2e6e6e2b.png)

## References
- [Expo iOS Build Docs](https://docs.expo.dev/classic/building-standalone-apps/#ios)
