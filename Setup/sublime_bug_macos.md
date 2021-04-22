Sometimes sublime crash in MacOS

Problem is the sublime linter plugin.

## Solution
Removing `~/Library/Caches/com.sublimetext.3` and also removing `~/Library/Application\ Support/Sublime\ Text\ 3` and reinstalling the package can do the trick.

```sh
rm -rf ~/Library/Caches/com.sublimetext.3
rm -rf ~/Library/Application\ Support/Sublime\ Text\ 3
sudo reboot # restarts the computer
```

## If not,
Configure the linter to trigger on save rather than background.
`shift + command + P` with Sublime opened.

`Preferences: SublimeLinter Settings`

add "lint_mode":  "save",in the User settings:
```
{
  "paths": {
    "linux": [
      "~/.rbenv/shims"
    ],
    "osx": [
      "~/.rbenv/shims"
    ]
  },
  "lint_mode": "save",
}
```
