# Troubleshooting
This is a repository with some frequently found problems and their solutions.

## Setup

[setup commmon errors](https://www.notion.so/Setup-Common-Errors-f09ad57cc4ae4a9a966b63dbf4e5620d).

[wsl cheatsheet](https://github.com/lewagon/setup/blob/master/wsl_cheatsheet.md).

## Javascript Week

### Node
```
Error: 
The following directories are not writable by your user:
/usr/local/share/zsh
/usr/local/share/zsh/site-functions
You should change the ownership of these directories to your user.
 sudo chown -R $(whoami) /usr/local/share/zsh /usr/local/share/zsh/site-functions
And make sure that your user has write permission.
 chmod u+w /usr/local/share/zsh /usr/local/share/zsh/site-functions

Fix:
sudo chown -R $(whoami) 
chmod u+w /usr/local/share/zsh
```

### Yarn

1. Error when installing on WSL
```
Error:
gpg: can't connect to the agent: IPC connect call failed

Fix:
sudo apt-get remove gpg
sudo apt-get install gnupg1
```

### Missing write access to /usr/local/lib/node_modules 

```
This permission fix might solve it:

sudo chown -R $USER /usr/local/lib/node_modules
```

[Source](https://flaviocopes.com/npm-fix-missing-write-access-error/)

### Rake Webpack CONNECTION REFUSED
[This fix solved it](https://github.com/webpack/webpack-dev-server/issues/1347).

To create the `alias` fix:

`echo " alias rake-webpack='../../node_modules/.bin/webpack-dev-server --mode development --host 0.0.0.0 --hot --open --useLocalIp' " >> ~/.zshrc`

To specify the port, just add `--port 3000`.

It'll look like `rake-webpack --port 1234`.

## AirBnb && Projects

### Install Heroku

Se der ruim, use isso:
`curl https://cli-assets.heroku.com/install-ubuntu.sh | sh`

### Cloudinary
- issue seeding pictures from Cloudinary

```
Error:
tempfile error (on Ubuntu). 

Fix:
item.individual_pieces.attach(
    io: open('https://res.cloudinary.com/dj9iphc8u/image/upload/v1597913613/outfit/o1_sweater_a94vol.png'),
    filename: 'o1_sweater_a94vol.png',
    content_type: 'image/png',
    identify: false
  )

Adding the identify: false fixed the issue
```

### Webpacker

- CSS and JS do not recompile after change
remove `public/assets` or `public/packs` folder.
