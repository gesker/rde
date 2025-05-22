# Assignment_Week_01-Assignment-3

## DevContainer Local

This devcontainer uses a Dockerfile

On the local machine ensure that Docker (container engine) is installed.

My local machine had PodMan installed instead of Docker so the following snippet was required in the `Library/Application\ Support/Code/User/settings.json` file:

```json
{
    ...
  "dev.containers.dockerPath": "podman"
    ...
}
```

## CodeSpaces Autoupdate Error

Disabling `autoupdate` helped get rid of error **SOME OF THE TIME**:

```bash
Installing platform package from https://github.com/vadimcn/codelldb/releases/download/v1.11.4/codelldb-linux-x64.vsix
Error: Error: command 'workbench.extensions.command.installFromVSIX' not found
```
