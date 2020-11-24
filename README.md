# Troubleshooting
This is a repository with some frequently found problems and their solutions.

## Setup

- [setup commmon errors](https://www.notion.so/Setup-Common-Errors-f09ad57cc4ae4a9a966b63dbf4e5620d).

- [wsl cheatsheet](https://github.com/lewagon/setup/blob/master/wsl_cheatsheet.md).

- download fstack repo again:

```
curl -s https://kitt.lewagon.com/camps/:CAMP_NUMBER/setup_script/:GITHUB_USERNAME | bash
```

## Javascript

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

- Node is on version 8, [how to delete it?](https://stackoverflow.com/questions/32426601/how-can-i-completely-uninstall-nodejs-npm-and-node-in-ubuntu-14-04)

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
remove `public/assets` and/or `public/packs` folder.

- Node is above 15 and webpacker breaks

On MacOS:
```
- brew install nvm
- restart the terminal
- nvm install 12.16.2
- node -v (to check they don't have the node v15 or something)
```

On Ubuntu:
TDB

### Mapbox-gl
[Uncaught ReferenceError: _typeof is not defined](https://github.com/andrerferrer/troubleshooting-lw/blob/master/mapbox-gl/Uncaught%20ReferenceError%20_typeof%20is%20not%20defined.md)


## Rails

### Testing on Rails

Testing wont work by default on WSL2. It requires ChromeDriver and Chrome binary installed. For this we will need the `root` session ( AKA The super-mega-admin-session ).

You may skip the reset of the password if you already have one for your root session.

Close all WSL2 tabs.
Open a Powershell tab and run the following command:
```bash
wsl -d Ubuntu -u root
```

You are now login in your Ubuntu as `root`.

Type the following command to change it's password:
```bash
passwd
```

You will be prompted twice for a new password.

Close this WSL2 tab.

Open a WSL2 tab, you should be logged in with **your** account. Run the following command (**line per line**):
```bash
sudo apt-get update
sudo apt-get install -y unzip xvfb libxi6 libgconf-2-4
```

We need to act as the `root` session for the next command, so let's login as root (you will be prompted for the `root` password):
```bash
su -
```
Now, let's run:
```bash
sudo curl -sS -o - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add
sudo echo "deb [arch=amd64]  http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list
```
Press `Ctrl+D` to quit the root session.

If you are unsure about which session you're logged in with, you can use the ```whoami``` command 💡.

Let's run the following commands to install Google Chrome binary and ChromeDriver on your WSL2:
```bash
sudo apt-get -y update
sudo apt-get -y install google-chrome-stable
wget https://chromedriver.storage.googleapis.com/2.41/chromedriver_linux64.zip
unzip chromedriver_linux64.zip
sudo mv chromedriver /usr/bin/chromedriver
sudo chown your-session-here:your-session-here /usr/bin/chromedriver
sudo chmod +x /usr/bin/chromedriver
```
⚠️ Replace **your-session-here** by the result of the command ```whoami```.
My result is ```barangerbenjamin:barangerbenjamin```. ⚠️

You can now use testing in Rails. You need to open a second tab and run:
```bash
chromedriver
```
In the other tab you can run your tests with:
```bash
rails test:system
```
