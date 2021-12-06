# graphiql Browser bundle bug

Doing a browser bundle using esbuild:

`esbuild --bundle --platform=browser --outdir=dist index.ts`

An error is shown:

```
✘ [ERROR] Could not resolve "punycode"

    node_modules/.pnpm/markdown-it@12.2.0/node_modules/markdown-it/lib/index.js:14:27:
      14 │ var punycode     = require('punycode');
         ╵                            ~~~~~~~~~~

  The package "punycode" wasn't found on the file system but is built into node. Are you trying to
  bundle for node? You can use "--platform=node" to do that, which will remove this error.

✘ [ERROR] Could not resolve "path"

    node_modules/.pnpm/picomatch@2.3.0/node_modules/picomatch/lib/picomatch.js:3:21:
      3 │ const path = require('path');
        ╵                      ~~~~~~

  The package "path" wasn't found on the file system but is built into node. Are you trying to
  bundle for node? You can use "--platform=node" to do that, which will remove this error.

✘ [ERROR] Could not resolve "path"

    node_modules/.pnpm/picomatch@2.3.0/node_modules/picomatch/lib/constants.js:3:21:
      3 │ const path = require('path');
        ╵                      ~~~~~~

  The package "path" wasn't found on the file system but is built into node. Are you trying to
  bundle for node? You can use "--platform=node" to do that, which will remove this error.

✘ [ERROR] Could not resolve "path"

    node_modules/.pnpm/picomatch@2.3.0/node_modules/picomatch/lib/utils.js:3:21:
      3 │ const path = require('path');
        ╵                      ~~~~~~

  The package "path" wasn't found on the file system but is built into node. Are you trying to
  bundle for node? You can use "--platform=node" to do that, which will remove this error.

4 errors
 ELIFECYCLE  Command failed with exit code 1.
```
