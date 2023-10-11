```
pnpm init
pnpm nuxt build
```

```
[nitro 10:06:53]  ERROR  Error: Transform failed with 1 error:
C:\Users\HYH\Desktop\bug\.nuxt\dist\server\_nuxt\login-817b54f8.js:2822:170: ERROR: The symbol "isError" has already been declared


The symbol "isError" has already been declared


[10:06:53]  ERROR  Transform failed with 1 error:
C:\Users\HYH\Desktop\bug\.nuxt\dist\server\_nuxt\login-817b54f8.js:2822:170: ERROR: The symbol "isError" has already been declared

  .nuxt\dist\server\_nuxt\login-817b54f8.js:2822:170: ERROR: The symbol "isError" has already been declared
  at failureErrorWithLog (node_modules\.pnpm\esbuild@0.19.4\node_modules\esbuild\lib\main.js:1650:15)
  at node_modules\.pnpm\esbuild@0.19.4\node_modules\esbuild\lib\main.js:848:29
  at responseCallbacks.<computed> (node_modules\.pnpm\esbuild@0.19.4\node_modules\esbuild\lib\main.js:703:9)
  at handleIncomingPacket (node_modules\.pnpm\esbuild@0.19.4\node_modules\esbuild\lib\main.js:763:9)
  at Socket.readFromStdout (node_modules\.pnpm\esbuild@0.19.4\node_modules\esbuild\lib\main.js:679:7)
  at Socket.emit (node:events:514:28)
  at addChunk (node:internal/streams/readable:343:12)
  at readableAddChunk (node:internal/streams/readable:316:9)
  at Readable.push (node:internal/streams/readable:253:10)
  at Pipe.onStreamRead (node:internal/stream_base_commons:190:23)
```