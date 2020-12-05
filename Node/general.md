[back](../README.md)

- On MacOs
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

- Node is on version 8 
    - [how to delete it?](https://stackoverflow.com/questions/32426601/how-can-i-completely-uninstall-nodejs-npm-and-node-in-ubuntu-14-04)
