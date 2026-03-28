Package: libedit:x64-linux@2024-08-08#1

**Host Environment**

- Host: x64-linux
- Compiler: GNU 15.2.1
- CMake Version: 3.31.11
-    vcpkg-tool version: 2026-03-04-4b3e4c276b5b87a649e66341e11553e8c577459c
    vcpkg-scripts version: b5d1a94fb7 2026-03-27 (21 hours ago)

**To Reproduce**

`vcpkg install `

**Failure logs**

```
libedit currently requires the following programs from the system package manager:
    autoconf autoheader aclocal automake libtoolize
On Debian and Ubuntu derivatives:
    sudo apt install autoconf libtool
On recent Red Hat and Fedora derivatives:
    sudo dnf install autoconf libtool
On Arch Linux and derivatives:
    sudo pacman -S autoconf automake libtool
On Alpine:
    apk add autoconf automake libtool
Downloading https://thrysoee.dk/editline/libedit-20240808-3.1.tar.gz -> libedit-20240808-3.1.tar.gz
Successfully downloaded libedit-20240808-3.1.tar.gz
-- Extracting source /home/artjomplaunov/vcpkg/downloads/libedit-20240808-3.1.tar.gz
-- Using source at /home/artjomplaunov/vcpkg/buildtrees/libedit/src/20240808-3-eb4c8bbbd6.clean
-- Getting CMake variables for x64-linux
-- Loading CMake variables from /home/artjomplaunov/vcpkg/buildtrees/libedit/cmake-get-vars_C_CXX-x64-linux.cmake.log
CMake Error at /home/artjomplaunov/sdb/build/vcpkg_installed/x64-linux/share/vcpkg-make/vcpkg_make.cmake:108 (message):
  libedit currently requires the following programs from the system package
  manager:

      autoconf autoconf-archive automake libtoolize

  

      On Debian and Ubuntu derivatives:
          sudo apt install autoconf autoconf-archive automake libtool
      On recent Red Hat and Fedora derivatives:
          sudo dnf install autoconf autoconf-archive automake libtool
      On Arch Linux and derivatives:
          sudo pacman -S autoconf autoconf-archive automake libtool
      On Alpine:
          apk add autoconf autoconf-archive automake libtool
      On macOS:
          brew install autoconf autoconf-archive automake libtool

Call Stack (most recent call first):
  /home/artjomplaunov/sdb/build/vcpkg_installed/x64-linux/share/vcpkg-make/vcpkg_make_configure.cmake:66 (vcpkg_run_autoreconf)
  ports/libedit/portfile.cmake:26 (vcpkg_make_configure)
  scripts/ports.cmake:206 (include)



```

**Additional context**

<details><summary>vcpkg.json</summary>

```
{
  "dependencies": [
    "libedit",
    "catch2"
  ]
}

```
</details>
