# Stack Assets Builder

built for [stack](https://github.com/creationix/stack) but can be used on its own

```js
var stack = require('stack')
require('http').createServer(stack(
  require('stack-assets-builder')({ enabled: true, root: __dirname }),
  require('stack-assets-static')({ root: __dirname })
))
```

options

 - enabled: boolean, should the builder be active? this can be changed on the passed-in object to toggle it
 - root: string, the path to look for the assets in

js files will be looked for under `root+'/src/*'` and hosted at `/js/*`
less files will be looked for under `root+'/less/*'` and hosted at `/css/*`