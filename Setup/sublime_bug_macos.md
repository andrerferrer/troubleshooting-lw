UNDER CONSTRUCTION


Problem is the sublime linter


Removing ~/Library/Caches/com.sublimetext.3
and also removing ~/Library/Application Support/Sublime Text 3 and reinstalling the packages did the trick



I found out that sublime crashes because of a memory leak caused by SublimeLinter package. A fix that is seems to work for me is to configure the linter to trigger on save rather than background.
shift + command + P
Preferences: SublimeLinter Settings
add "lint_mode":  "save",in the User settings
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
