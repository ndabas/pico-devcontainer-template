# Sample Pico SDK project for toolchain installation with vcpkg

This project contains configuration to allow fully automated toolchain installation with [vcpkg artifacts](https://devblogs.microsoft.com/cppblog/vcpkg-artifacts/) (also known as vcpkg-ce in some documentation.)

While vcpkg supports installation on Linux, macOS, and Windows, the current set of packages are only published for Windows.

To try it out:
1. Download or clone this project to your computer.
1. Open the folder in Visual Studio Code.
1. Visual Studio Code might be very excited to see the project and start throwing all sorts of errors and messages. Ignore everything.
1. Except for the message that asks you if you would like to install the workspace recommended extensions. Answer yes to that one and wait until all of the extensions are installed.
1. When all the extensions are installed, you will see a "vcpkg" button on the status bar with a spinner indicating progress. Click it to see the log.
1. When it is done, you will see a message like: "Activated environment at ...".
1. You can now click the CMake button on the Visual Studio Code navigation bar to open the CMake project outline.
1. Click the three dots button on top of the outline, and choose to Clean Reconfigure All Projects.
1. When done, you can click the small Build All Projects button to start the actual build.

## Configuration
You can look through, and copy to your own projects, the configuration files that make this work:
- [vcpkg-configuration.json](vcpkg-configuration.json)
- [CMakePresets.json](CMakePresets.json)
- Several files in [.vscode](.vscode)

## What it does
vcpkg artifacts downloads and extracts the toolchain to the location specified in [.vscode/settings.json](.vscode/settings.json), on this line:
```
"vcpkg.storageLocation": "C:/vcpkg"
```
Change this to modify where the downloaded files are stored. You can simply delete this directory to "uninstall" the toolchain. Note that this must be a relatively short path, as GCC and the other tools might have trouble locating certain files if the path lengths become too long.

vcpkg artifacts will also set up the correct PATH and other environment variables within Visual Studio Code, without making any changes to the global environment or registry.
