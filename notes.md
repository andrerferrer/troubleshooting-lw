https://github.com/v-natalia/setup-fixes/blob/master/fixes.md#vs-code-connection-to-ubuntu

---------------

Starting directories were ALL WRONG

---------------


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
VScode connection
https://github.com/andrerferrer/troubleshooting-lw/blob/master/VS%20Code%20connection%20to%20Ubuntu.md#vs-code-connection-to-ubuntu


--------------

![image](https://user-images.githubusercontent.com/45776359/148555671-055a9f87-a8b2-4158-8cf7-e6a242be3aae.png)
```
> sudo apt-get update
Err:1 http://security.ubuntu.com/ubuntu bionic-security InRelease
  Temporary failure resolving 'security.ubuntu.com'
Err:2 http://archive.ubuntu.com/ubuntu bionic InRelease
  Temporary failure resolving 'archive.ubuntu.com'
Err:3 http://archive.ubuntu.com/ubuntu bionic-updates InRelease
  Temporary failure resolving 'archive.ubuntu.com'
Err:4 http://archive.ubuntu.com/ubuntu bionic-backports InRelease
  Temporary failure resolving 'archive.ubuntu.com'
Reading package lists... Done
W: Failed to fetch http://archive.ubuntu.com/ubuntu/dists/bionic/InRelease  Temporary failure resolving 'archive.ubuntu.com'
W: Failed to fetch http://archive.ubuntu.com/ubuntu/dists/bionic-updates/InRelease  Temporary failure resolving 'archive.ubuntu.com'
W: Failed to fetch http://archive.ubuntu.com/ubuntu/dists/bionic-backports/InRelease  Temporary failure resolving 'archive.ubuntu.com'
W: Failed to fetch http://security.ubuntu.com/ubuntu/dists/bionic-security/InRelease  Temporary failure resolving 'security.ubuntu.com'
W: Some index files failed to download. They have been ignored, or old ones used instead.
```

https://stackoverflow.com/questions/60269422/windows10-wsl2-ubuntu-debian-no-network

------------------

![image](https://user-images.githubusercontent.com/45776359/148558965-01719c46-4b2a-43b8-8fcc-f009ce94a29e.png)

```
key=40976EAF437D05B5
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys $key
```
https://github.com/cli/cli/issues/1799
https://chrisjean.com/fix-apt-get-update-the-following-signatures-couldnt-be-verified-because-the-public-key-is-not-available/


-----------------------
