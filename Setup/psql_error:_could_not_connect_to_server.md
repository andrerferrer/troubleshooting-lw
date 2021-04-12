```
brew uninstall --force postgres
rm -rf /usr/local/var/postgres
rm -rf .psql_history .psqlrc .psql.local .pgpass .psqlrc.local
brew cleanup
```

Then, run it and nothing should show up

`brew list | grep sql`

If nothing showed up,

`brew install postgresql`
`brew services start postgresql`

After that

`psql -d postgres`
