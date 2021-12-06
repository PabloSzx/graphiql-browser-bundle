# graphiql Browser bundle bug

Doing a browser bundle using esbuild:

`esbuild --bundle --platform=browser index.ts --outdir=dist`

An error is shown:

```
✘ [ERROR] Could not resolve "punycode"

    node_modules/.pnpm/markdown-it@12.2.0/node_modules/markdown-it/lib/index.js:14:27:
      14 │ var punycode     = require('punycode');
         ╵                            ~~~~~~~~~~

  The package "punycode" wasn't found on the file system but is built into node. Are you trying to
  bundle for node? You can use "--platform=node" to do that, which will remove this error.

✘ [ERROR] Could not resolve "react-dom"

    node_modules/.pnpm/graphiql@1.5.12_3f0ff33733f491c0a940f2d793f7984e/node_modules/graphiql/esm/components/ResultViewer.js:15:21:
      15 │ import ReactDOM from 'react-dom';
         ╵                      ~~~~~~~~~~~

  You can mark the path "react-dom" as external to exclude it from the bundle, which will remove
  this error.

✘ [ERROR] Could not resolve "path"

    node_modules/.pnpm/picomatch@2.3.0/node_modules/picomatch/lib/picomatch.js:3:21:
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

✘ [ERROR] Could not resolve "path"

    node_modules/.pnpm/picomatch@2.3.0/node_modules/picomatch/lib/constants.js:3:21:
      3 │ const path = require('path');
        ╵                      ~~~~~~

  The package "path" wasn't found on the file system but is built into node. Are you trying to
  bundle for node? You can use "--platform=node" to do that, which will remove this error.

5 errors
 ELIFECYCLE  Command failed with exit code 1.

```
