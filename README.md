# React-native-android-vagrant

Basic vagrant project to orchestrate a react-native android development environment.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine.

### Prerequisites

Make sure you have vagrant up and running on your local machine.

## Deployment

If you are on windows make sure to open your terminal as admin.

```
vagrant up
```
```
vagrant ssh
```

## React Native Project

Make sure you are located in the shared folder.

```
cd vagrant_sync
```

### Create a new project

Just create a project like you normally do.

```
react-native init [project-name]
```

### Run a project

Make sure you have your device plugged in to the VM and in development mode.

```
react-native run-android
```
```
react-native start
```

### Android device

To connect your device:
- Connect a phone to the VM.
- Kill adb server if is running.

```
/opt/adt/android-sdk-linux/platform-tools/adb kill-server
```

- Start adb server as sudo.

```
sudo /opt/adt/android-sdk-linux/platform-tools/adb start-server
```

- Allow the connection on the phone.
- Allow the connection on the phone.
- See if connection is ok.

```
/opt/adt/android-sdk-linux/platform-tools/adb devices
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details.
