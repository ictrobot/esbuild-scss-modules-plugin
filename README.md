esbuild-scss-modules-plugin
=======

Plugin to use scss and css modules with esbuild.
Based on [indooorsman/esbuild-css-modules-plugin](https://github.com/indooorsman/esbuild-css-modules-plugin/blob/eff4a500c56a45b1550887a8f7c20f57b01a46b7/index.js).

![npm](https://img.shields.io/npm/v/esbuild-scss-modules-plugin)

## Example

```js
import esbuild from "esbuild";
import {ScssModulesPlugin} from "esbuild-scss-modules-plugin";

const result = await esbuild.build({
    entryPoints: ['src/index.ts'],
    bundle: true,
    outfile: 'dist/index.js',

    plugins: [
        ScssModulesPlugin({
            inject: false,
            minify: true,
            cssCallback: (css) => console.log(css),
        })
    ]
})
```

## Options
See `index.ts`

## License
MIT
