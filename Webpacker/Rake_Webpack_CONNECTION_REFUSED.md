[back](../README.md)

[This fix solved it](https://github.com/webpack/webpack-dev-server/issues/1347).

To create the `alias` fix:

`echo " alias rake-webpack='../../node_modules/.bin/webpack-dev-server --mode development --host 0.0.0.0 --hot --open --useLocalIp' " >> ~/.zshrc`

To specify the port, just add `--port 3000`.

It'll look like `rake-webpack --port 1234`.