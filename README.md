# mfgfix-ae

## Dependencies
- CommonLibSSE
- Detours
## How to build
#### Prerequisites
- Visual Studio 2019
- vcpkg (for CommonLibSSE)

Open x64 Native Tools Command Prompt for VS 2019.

Clone repository:
```
git clone https://github.com/andrelo1/mfgfix-ae
cd mfgfix-ae
```
Clone and build CommonLibSSE:
```
git clone https://github.com/Ryan-rsm-McKenzie/CommonLibSSE
cd CommonLibSSE
cmake -B build -S . -DCMAKE_TOOLCHAIN_FILE=[path to vcpkg]/scripts/buildsystems/vcpkg.cmake -DVCPKG_TARGET_TRIPLET=x64-windows-static-md
cd ..
```
Clone and build Detours:
```
git clone https://github.com/microsoft/Detours
cd Detours/src
nmake
```
Open `mfgfix.sln` in Visual Studio and build solution.
