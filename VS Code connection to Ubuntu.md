## VS Code connection to Ubuntu

### [Connecting VS Code to Ubuntu](https://github.com/lewagon/setup/blob/master/windows.md#connecting-vs-code-to-ubuntu)

It should connect actomatically to WSL-Ubuntu but it doesn't. To fix this, install manually the extension WSL.
For that, open VS Code and go to the small square on the left that allows to install extensions.
![extensions](images/extensions.png 'Install extensions').


There, search for Remote-WSL and install it (image below for reference).


![install WSL extension](images/installremote-wsl.png 'Install WSL extension')


After that, click on the small computer (menu on the left) to connect Ubuntu to VS Code
![connect Ubuntu](images/connectubuntu.png 'Connect Ubuntu').

Where it says WSL targets, click on the button with a '+' that appears on the right of the name of the Ubuntu distro.
![add Ubuntu](images/ubuntu.png 'Connect Ubuntu').

Then, the magic operates and VS Code will be connected to Ubuntu.
