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

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
