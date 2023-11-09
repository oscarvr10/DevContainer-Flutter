# Flutter Local Dev Environment with Docker

This repository is a template for mount a local environment for work with Flutter inside a container.

# Credits

Thanks to Mats Pfeiffer for his contribution. Original repo can be found [here:]( https://github.com/matsp/docker-flutter/tree/master)

## Installation requirements and Usage

1. Install [Docker](https://www.docker.com/get-started/) in your machine.
2. Install [Visual Studio Code](https://code.visualstudio.com/).
3. Install [Dev Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) in Visual Studio Code.
4. Open this project in Visual Studio Code, then select 'Open in Dev Container' option.
5. Enjoy!.

## Wireless debugging

### Linux

1. Connect your Android device via USB before to open the dev container.
2. Connect your device via USB and make sure debugging is enabled, then run:

```sh
adb tcpip 5555
```

3. Find the IP address of your device, go to Settings > Wi-Fi > Advanced > IP Address on your device or run `adb shell netcfg`.
4. Connect to device using the IP address with the following command:

```sh
adb connect xxx.xxx.x.x
```

5. Disconnect your device from USB and proceed with wireless debugging.

> Troubleshooting: You can try kill the adb daemon in your host machine using the command `abd kill-server` and then your container should have access to list the device.

### Windows and MacOS

1. Start your local android emulator. Afterwards reconnect execute the following command to make it accessable via network:

```shell
adb tcpip 5555
```

2. In your docker container connect to device:

```shell
adb connect host.docker.internal:5555
```

3. You can now choose the device to start debugging.


## Contributing

Contributions are always welcome!

## Sources

- [Developing inside a Container Vscode](https://code.visualstudio.com/docs/remote/containers#_getting-started)
- [Enable adb debugging on your device](https://developer.android.com/studio/command-line/adb#Enabling)
