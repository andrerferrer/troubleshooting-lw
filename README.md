# Troubleshooting
This is a repository with some frequently found problems and their solutions.

## Setup

[setup commmon errors](https://www.notion.so/Setup-Common-Errors-f09ad57cc4ae4a9a966b63dbf4e5620d).

[wsl cheatsheet](https://github.com/lewagon/setup/blob/master/wsl_cheatsheet.md).

## Javascript Week

### Javascript-basics

#### Missing write access to /usr/local/lib/node_modules [Source](https://flaviocopes.com/npm-fix-missing-write-access-error/)

This permission fix might solve it:

`sudo chown -R $USER /usr/local/lib/node_modules`