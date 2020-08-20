# Troubleshooting
This is a repository with some frequently found problems and their solutions.

## Setup

[setup commmon errors](https://www.notion.so/Setup-Common-Errors-f09ad57cc4ae4a9a966b63dbf4e5620d).

[wsl cheatsheet](https://github.com/lewagon/setup/blob/master/wsl_cheatsheet.md).

## Javascript Week

### Yarn

1. Error when installing on WSL
```
Error:
gpg: can't connect to the agent: IPC connect call failed

Fix:
sudo apt-get remove gpg
sudo apt-get install gnupg1
```


### Javascript-basics

#### Missing write access to /usr/local/lib/node_modules 

```
This permission fix might solve it:

sudo chown -R $USER /usr/local/lib/node_modules
```

[Source](https://flaviocopes.com/npm-fix-missing-write-access-error/)

#### Rake Webpack CONNECTION REFUSED
[This fix solved it](https://github.com/webpack/webpack-dev-server/issues/1347).

To create the `alias` fix:

`echo " alias rake-webpack='../../node_modules/.bin/webpack-dev-server --mode development --host 0.0.0.0 --hot --open --useLocalIp' " >> ~/.zshrc`

To specify the port, just add `--port 3000`
