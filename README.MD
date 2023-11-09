# Dev Container for Flutter with Docker

This repository is a template for mount a local environment for work with Flutter inside a container.

# Credits

Thanks to Mats Pfeiffer for his contribution. Original repo can be found [here:]( https://github.com/matsp/docker-flutter/tree/master)

## Installation requirements and Usage

1. Install [Docker](https://www.docker.com/get-started/) in your machine.
2. Install [Visual Studio Code](https://code.visualstudio.com/).
3. Install [Dev Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) in Visual Studio Code.
4. Open this project in Visual Studio Code, then select 'Open in Dev Container' option.
5. Enjoy!.

## Debugging with Android Emulator

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
