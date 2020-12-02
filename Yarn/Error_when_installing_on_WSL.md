[back](../README.md)

#### Error when installing on WSL
```
Error:
gpg: can't connect to the agent: IPC connect call failed

Fix:
sudo apt-get remove gpg
sudo apt-get install gnupg1
```