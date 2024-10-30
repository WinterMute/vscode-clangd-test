We're currently working on figuring out how to get code completion via clangd working cross platform while allowing the vscode project settings to be shared.

This project will work across macOS, linux and windows with the caveat that vscode should be started from the msys2 shell after running `make GENERATE_COMPILE_COMMANDS=1`

The issue we currently have is that [this line](https://github.com/WinterMute/vscode-clangd-test/blob/main/.vscode/settings.json#L9) will only work on windows if the environment variable gets translated into a windows path (which the msys2 shell will do when starting a native windows program)

This may not matter if you don't use windows. It makes things kind of awkward if you do.

![image](https://github.com/user-attachments/assets/b8f8bd41-513d-43e6-8f2a-b79ebc56d85b)
