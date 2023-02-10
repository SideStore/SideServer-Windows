# SideServer for Windows

In order to compile SideServer on VS 2019/2022 there a few things required.
Install the installer plugin that match your VS version from [here](https://marketplace.visualstudio.com/items?itemName=VisualStudioClient.MicrosoftVisualStudio2017InstallerProjects).

1. clone the repository **recursively** and checkout the `error_handling` branch
2. install and bootstrap [VCPKG](https://github.com/microsoft/vcpkg)
3. In the `Dependencies\libimobiledevice-vs` folder, run the `./get-source` script to download the source repos
4. In the project `imobiledevice`:
    - Open the project properties page
    - Navigate to `Configuration Properties > vcpkg`
    - Turn on `Use Vcpkg Manifest`
5. In `AltServer` and `AltSign`, change the toolset to `v143` (if using VS2022)

The code should now compile, but only in x86 for now.

### To Do

- [ ] Fix x64 build??
- [ ] Add pairing file support (commented out, some module error)
- [ ] Rebrand AltServer to SideServer
- [ ] Add beta build install option
