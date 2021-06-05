Having to enter your password each time you try and push to github :github:. 

Here is a fix for that :sorriso_olhos_sorrindo::apontando_para_baixo:
Mac :macos_sierra:

:símbolo_informações: you will need to create (touch) a file, open it and paste some code inside (configurations)

if you take the code below and run this in your terminal
```
touch ~/.ssh/config  
st ~/.ssh/config    
```
and then add this to that file:
```
Host *
  AddKeysToAgent yes
  UseKeychain yes
 ```
and dont forget to save!
