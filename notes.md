![Untitled](https://user-images.githubusercontent.com/45776359/148554395-416581b4-0434-4cfa-afab-a911ed694cf2.png)

`sudo dpkg -i --force-all /var/cache/apt/archives/gh_2.4.0_amd64.deb`


-----------------

[TROUBLESHOOTING]If you got the .bin/readlink no such file or directory  for data and web students while downloading pyenv or rbenv, please remove from the settings.json the line
"startingDirectory" 
and add instead,
"commandline": "wsl.exe ~"
restart the terminal and try again the download


credits to @natalia

--------------
