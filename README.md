<!--
SPDX-FileCopyrightText: 2026 DioEgizio

SPDX-License-Identifier: BSD-2-Clause
-->

## Qt builds (for Prism Launcher)

This repository builds Qt through GitHub Actions with the intent of, at one point, being the Qt build used in Prism Launcher.

### Usage in GitHub Actions workflows

```yaml
    - name: Install Qt
      uses: DioEgizio/qtbuild@6.12
      with:
        version: 6.12.0 # the version of Qt
        preset: Linux # the preset to install
```

You can take a look at releases for the available versions, for the presets:
- `Linux` is for amd64 linux
- `Linux-aarch64` is for arm64 linux
- `macOS` is for (universal) macOS
- `Windows-MSVC` is for amd64 Windows with the MSVC toolchain
- `Windows-MSVC-arm64` is for arm64 Windows with the MSVC toolchain
- `Windows-MinGW-w64` is for amd64 Windows with the LLVM (clang, libc++, libunwind) toolchain in MinGW-w64 mode
