[Back](https://github.com/andrerferrer/troubleshooting-lw)

Might be because Sublime Linter doesn't know the path to node

`which node` and copy the path (without node). Something like `/home/andrerferrer/.nvm/versions/node/v14.15.0/bin`.

Open the Sublime Linter settings and add the path:

```
"paths": 
  {
    "osx": ["/home/andrerferrer/.nvm/versions/node/v14.15.0/bin"]
  },
"linters": {
    "eslint": {
      "env": {"PATH": "~/.nvm/versions/node/v8.11.4/bin"}
    }
```

[Source](https://github.com/SublimeLinter/SublimeLinter/issues/1118#issuecomment-393030063).
[Source2](https://github.com/SublimeLinter/SublimeLinter/issues/1318).
