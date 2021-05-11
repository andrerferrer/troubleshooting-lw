Might be because Sublime Linter doesn't know the path to node

`which node` and copy the path (without node). Something like `/home/andrerferrer/.nvm/versions/node/v14.15.0/bin`.

Open the Sublime Linter settings and add the path:

```
"paths": {
		"osx": ["/home/andrerferrer/.nvm/versions/node/v14.15.0/bin"]
	}
```

[Source](https://github.com/SublimeLinter/SublimeLinter/issues/1118#issuecomment-393030063).
