## Solution

Add to `# config/webpack/environment.js`:

```
environment.loaders.delete('nodeModules')
```


## References:

https://github.com/mapbox/mapbox-gl-js/issues/8574


https://github.com/mapbox/mapbox-gl-js/issues/3422