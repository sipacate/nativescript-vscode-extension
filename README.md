NativeScript Extension for Visual Studio Code
========

### Introduction

The NativeScript extension for Visual Studio Code aids your [NativeScript](https://www.nativescript.org/) project development within Visual Studio Code.

### Install NativeScript

To install [NativeScript](https://www.nativescript.org/) and all its dependencies, follow the instructions in our [getting started guide](http://docs.nativescript.org/start/getting-started#getting-up-and-running).

### Setup the extension

Create NativeScript application by running `tns create MyApp` and open `MyApp` folder in Visual Studio Code. Open the Debug Panel, click the gear icon

![gear icon](https://raw.githubusercontent.com/NativeScript/nativescript-vscode-extension/master/images/screenshots/nativescript-gear-icon.jpg)

and choose NativeScript debug environment.

![NativeScript debug settings](https://raw.githubusercontent.com/NativeScript/nativescript-vscode-extension/master/images/screenshots/nativescript-debug-settings.png)

### Debug your NativeScript application

To start the application with attached debugger, choose one of the launch configurations from the drop-down list and then click the start button.

![Launch settings](https://raw.githubusercontent.com/NativeScript/nativescript-vscode-extension/master/images/screenshots/nativescript-launch-configurations.png)

Your application will be launched and the VSCode debugger will break on the first JavaScript statement. Click continue and your app will show up on the emulator/device. If you want to attach to already running NativeScript application, use one of the attach configurations. More information on what you can do with the Visual Studio Code Debugger you can find [here](https://code.visualstudio.com/docs/editor/debugging).

### NativeScript commands

Type `NativeScript` in the Command Palette and you will see all available commands. 

![NativeScript Commands](https://raw.githubusercontent.com/NativeScript/nativescript-vscode-extension/master/images/screenshots/nativescript-commands.png)

There's only a couple of them but the list will grow in the future.

The `Run` command triggers `tns run` on emulator or device. You can run your app both on iOS and Android.

If your version of NativeScript is incompatible with the extension you will see a warning the first time you run a command.

### Get the latest bits

1. Clone the [extension repository](https://github.com/NativeScript/nativescript-vscode-extension): `git clone git@github.com:NativeScript/nativescript-vscode-extension.git`
2. To build the extension run the following commands in the root repository folder

    ```
    npm install # installs npm dependencies
    ./node_modules/.bin/tsd install # fetches TypeScript definitions
    ./node_modules/.bin/gulp # Builds the extension and produces 'out' folder
    ./node_modules/.bin/vsce package # produces nativescript-*.*.*.vsix in the root folder
    ```

3. To install the extension drag and drop the `nativescript-*.*.*.vsix` package in the VS Code.
