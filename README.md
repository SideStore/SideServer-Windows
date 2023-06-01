# SideServer for Windows

In order to compile SideServer on VS 2019/2022 (not tested on any earlier versions), ensure you have the correct environment then follow the steps below.

**Dev Environment**
- Ensure your Visual Studio installation has all the following:
  - The `Desktop development with C++` set of tools
  - `MSBuild support for LLVM (clang-cl) toolset`
  - `C++ Clang Compiler for Windows`
  - `Test Adapter for Boost.Test`
  - `C++ MFC for latest v143 build tools (x86 & x64)` (or v142)
- Bootstrapped and Integrated  [VCPKG](https://github.com/microsoft/vcpkg) package manager setup.
- Installer projects plugin that matches your VS version - [VS2017/2019](https://marketplace.visualstudio.com/items?itemName=VisualStudioClient.MicrosoftVisualStudio2017InstallerProjects), [VS2022](https://marketplace.visualstudio.com/items?itemName=VisualStudioClient.MicrosoftVisualStudio2022InstallerProjects).

**Build Instructions**
1. Clone the repository **recursively** (or run `git submodule update --init --recursive` after pull).
2. In the `Dependencies\libimobiledevice-vs` folder, run the `./get-source` script to download the libimobiledevice source repos
3. If using VS2022, in the `AltServer` and `AltSign` projects, change the MSVC toolset to `v143` (note that the migration tool may do this for you).
4. Compile (x86 only - the project won't work in x64).

### To Do

- [x] Add pairing file support (commented out, some module error)
- [x] Rebrand AltServer to SideServer
- [ ] Add release channels and correct IPA links
- [ ] Testing with users
