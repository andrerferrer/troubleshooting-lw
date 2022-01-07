# Troubleshooting
This is a repository with some frequently found problems and their solutions.

## Setup

- [setup common errors](https://www.notion.so/Setup-Common-Errors-f09ad57cc4ae4a9a966b63dbf4e5620d).

- [apple m1](https://github.com/lewagon/setup/blob/master/apple_m1_cheatsheet.md)

- [NVM issues](NVM/nvm.md)

- download fstack repo again with
    ```
    curl -s https://kitt.lewagon.com/camps/:CAMP_NUMBER/setup_script/:GITHUB_USERNAME | bash
    ```

    ### MacOs
- [Shallow clone issues](Setup/shallow_clone.md)
- [Terminal doesnt open rosetta](Setup/terminal_doesnt_open_rosetta.md)
- [psql: error: could not connect to server](Setup/psql_error_could_not_connect_to_server.md) 
- [GEM::FilePermissionError](Setup/gem_filepermissionerror.md) 
- [macOs_asks_for_gh_password](Setup/macOs_asks_for_gh_password.md) 

    ### WSL
- [LW cheatsheet](https://github.com/lewagon/setup/blob/master/docs/windows_cheatsheet.md)
- [Visual Studio Code tries to access old version of WSL](Setup/old_version_wsl.md)
- [wsl cheatsheet](https://github.com/andrerferrer/wsl_cheatsheet).
- [Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS](https://www.configserverfirewall.com/windows-10/please-enable-the-virtual-machine-platform-windows-feature-and-ensure-virtualization-is-enabled-in-the-bios/)
- [Cant install ubuntu because of microsoft store](https://stackoverflow.com/questions/52512026/is-it-possible-install-ubuntu-in-windows-10-wsl-without-microsoft-store)

Follow [this guide](https://docs.microsoft.com/en-us/windows/wsl/install-on-server).

The command to download is
`Invoke-WebRequest -Uri https://aka.ms/wslubuntu -OutFile Ubuntu.appx -UseBasicParsing`

- [Cant install terminal preview because of microsoft store](https://github.com/microsoft/terminal/releases)
- [WslRegisterDistribution_failed_witherror:_0xc03a001a](https://github.com/andrerferrer/wsl_cheatsheet/blob/master/WslRegisterDistribution_failed_witherror:_0xc03a001a.md)

## Javascript

### [Node](Node/general.md)

1. [Eslint not working](Node/eslint_not_working.md)

### Yarn

1. [Error when installing on WSL](Yarn/Error_when_installing_on_WSL.md)

### [Missing write access to /usr/local/lib/node_modules](Missing_write_access_to_usr-local-lib-node_modules.md)

### [Rake Webpack CONNECTION REFUSED](Webpacker/Rake_Webpack_CONNECTION_REFUSED.md)

## AirBnb && Projects

### Install heroku with alternative link

`curl https://cli-assets.heroku.com/install-ubuntu.sh | sh`

### [Cloudinary](Cloudinary/general.md)


### [Webpacker](Webpacker/general.md)


### Mapbox-gl
[Uncaught ReferenceError: _typeof is not defined](mapbox-gl/Uncaught_ReferenceError_typeof_is_not_defined)


## Rails

### [Testing on Rails](Rails/Testing_on_Rails.md)

### Turbolinks

- [Turbolinks back button on browser fix](https://github.com/andrerferrer/quickTips/blob/master/Rails/Turbolinks%20back%20button%20on%20browser%20fix.md)

### [PostgreSQL](PostgreSQL/general.md)
