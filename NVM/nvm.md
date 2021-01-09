- `zsh: command not found nvm `

    `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash`
    if it says no directory .nvm,  run `cd && mkdir .nvm`
    and run the curl command again. 
    
    Once it’s done QUIT your terminal and run `nvm -v`
    if it works you can finally run `nvm install 14.15.0` and checked that it worked with `node -v`

  Other sources:
    - [nvm install problems on macos](https://gist.github.com/juliends/e64c3bcd2d60cbae2f648958fb691e41)
    - [nvm instalation](https://stackoverflow.com/questions/16904658/node-version-manager-install-nvm-command-not-found)


