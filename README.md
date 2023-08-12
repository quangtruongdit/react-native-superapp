# react-native-superapp
React Native Super App using Re.Pack

## Usage

Clone project with sub modules:
```bash
git clone --recursive -j8 https://github.com/quangtruongdit/react-native-superapp.git
```

Install dependencies:

```bash
yarn bootstrap
```

Pod install iOS *(Only for iOS)*

```bash
yarn pod-install
```

Start development servers separately:

```bash
# todo:: configure with yarn workspace
yarn start:app1
yarn start:app2
yarn start:host
```

Remember to reverse port when run on real android device:

```bash
# for host app
adb -s {your android device name} reverse tcp:8081 tcp:8081
# for app1
adb -s {your android device name} reverse tcp:8083 tcp:8083
# for app2
adb -s {your android device name} reverse tcp:8084 tcp:8084
```

You may got an issue with android sdk is not set in local.properties. Try to do gradle sync your host app if this issue shows on console log.
```bash
cd ./rn-super-app/android
# make sure gradle is installed before using it
gradle build
```

Run Host app:

```bash
yarn run:host:ios
yarn run:host:android
```

Run Standalone:
```bash
# App One
yarn run:app1:ios
yarn run:app1:android

# App Two
yarn run:app2:ios
yarn run:app2:android
```

Demo:

![iOS Demo App](https://miro.medium.com/v2/resize:fit:592/1*m2-9ahLJkGZI6sy6Jq8QWg.gif)
