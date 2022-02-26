# rust-analyzer-arm
[![Compile Rust-Analyzer for ARMv7 (Raspberry Pi 2+)](https://github.com/Ardelean-Calin/rust-analyzer-arm/actions/workflows/rust-analyzer-compile.yml/badge.svg?branch=main)](https://github.com/Ardelean-Calin/rust-analyzer-arm/actions/workflows/rust-analyzer-compile.yml)

The rust-analyzer language server compiled for the ARMv7 instruction set.

This repository contains a single **Github Workflow** which fetches the latest [rust-analyzer](https://github.com/rust-analyzer/rust-analyzer) release and compiles it for ARMv7.
Currently this workflow runs daily, not on pull request, but this may be improved in the future.

To download the latest release use the following command:

**Option 1 - only curl:**

`curl https://api.github.com/repos/ardelean-calin/rust-analyzer-arm/releases/latest | grep "browser_download_url" | grep -Eo 'https://[^\"]*' | xargs curl -Ls -o rust-analyzer.zip -w %{url_effective}`

**Option 2 - curl + wget:**

`curl https://api.github.com/repos/ardelean-calin/rust-analyzer-arm/releases/latest | grep "browser_download_url" | grep -Eo 'https://[^\"]*' | xargs wget`
