# Troubleshooting
This is a repository with some frequently found problems and their solutions.



## Javascript Week

### Javascript-basics

#### Missing write access to /usr/local/lib/node_modules [Source](https://flaviocopes.com/npm-fix-missing-write-access-error/)

This permission fix might solve it:

`sudo chown -R $USER /usr/local/lib/node_modules`