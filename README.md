# msix-nsis

A mixed demo for wrapping the msix to NSIS(Nullsoft Scriptable Install System) setup program.

It make you can pack your `.msixbundle` and `.cer` files to a single setup program.

> Format appx/appxbundle/msix/msixbundle are supported.

## Features

- [x] Support auto install your certificate file using certmgr.

- [x] Support powerful NSIS script for expanding other functions.

## Usages

1. Solution File `msix/App.sln` is a WPF desktop program demo.

   To `publish` the `msix\App.Packaging\App.Packaging.wapproj` project and then get a testing msix package.

2. Copy the output `.msixbundle` and `.cer` files like [msix_build.bat](msix_build.bat).

   If publish output a `.msix` extension or other msix-like file, change the [nsis/setup.nsi](nsis/setup.nsi) file for supporting.

3. Build the NSIS setup like [nsis_build.bat](nsis_build.bat).

## Components

This demo including following components.

```bash
# https://docs.microsoft.com/en-us/dotnet/framework/tools/certmgr-exe-certificate-manager-tool
certmgr

# https://nsis.sourceforge.io
nsis

# https://github.com/emako/msixexec
msixexec
```

## FAQs

1. Unrecommended to replace the NSIS version in this demo.
3. UAC permission is required because certificate file should be auto installed.

