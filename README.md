# rust-analyzer-arm
The rust-analyzer language server compiled for the ARMv7 instruction set.

This repository contains a single **Github Workflow** which fetches the latest [rust-analyzer](https://github.com/rust-analyzer/rust-analyzer) release and compiles it for ARMv7.
Currently this workflow runs daily, not on pull request, but this may be improved in the future.

To download the latest release use the following command:

`curl https://api.github.com/repos/ardelean-calin/rust-analyzer-arm/releases/latest | grep "browser_download_url" | grep -Eo 'https://[^\"]*' | xargs wget`
