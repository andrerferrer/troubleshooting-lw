```
"This restriction has been made on GitHub's request because updating shallow
clones is an extremely expensive operation due to the tree layout and traffic of
Homebrew/homebrew-core and Homebrew/homebrew-cask. We don't do this for you
automatically to avoid repeatedly performing an expensive unshallow operation in
CI systems (which should instead be fixed to not use shallow clones). Sorry for
the inconvenience!"
```

after `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

We fixed it with a
```
git -C "/usr/local/Homebrew/Library/Taps/homebrew/homebrew-core" fetch --unshallow
git -C "/usr/local/Homebrew/Library/Taps/homebrew/homebrew-cask" fetch --unshallow
```

Sources:

* https://github.com/Homebrew/brew/issues/9420
* https://stackoverflow.com/questions/65160625/cant-update-or-upgrade-homebrew
