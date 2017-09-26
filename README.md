* Reproducer for issue: https://github.com/yarnpkg/yarn/issues/4539

With yarn 1.1.0 see tsutils has the typescript realised in its node_modules

```
find . -iname "*typescript*"
./node_modules/highlight.js/lib/languages/typescript.js
./node_modules/typedoc/node_modules/typescript
./node_modules/typedoc/node_modules/typescript/lib/typescript.d.ts
./node_modules/typedoc/node_modules/typescript/lib/typescriptServices.d.ts
./node_modules/typedoc/node_modules/typescript/lib/typescript.js
./node_modules/typedoc/node_modules/typescript/lib/typescriptServices.js
./node_modules/typedoc/dist/lib/utils/options/sources/typescript.d.ts
./node_modules/typedoc/dist/lib/utils/options/sources/typescript.js
./node_modules/typedoc/dist/lib/utils/options/sources/typescript.js.map
./node_modules/tsutils/node_modules/typescript
./node_modules/tsutils/node_modules/typescript/lib/typescript.d.ts
./node_modules/tsutils/node_modules/typescript/lib/typescriptServices.d.ts
./node_modules/tsutils/node_modules/typescript/lib/typescript.js
./node_modules/tsutils/node_modules/typescript/lib/typescriptServices.js
./node_modules/typescript
./node_modules/typescript/lib/typescript.d.ts
./node_modules/typescript/lib/typescriptServices.d.ts
./node_modules/typescript/lib/typescript.js
./node_modules/typescript/lib/typescriptServices.js
```

It does not with 1.0.2

```
 find . -iname "*typescript*"
./node_modules/highlight.js/lib/languages/typescript.js
./node_modules/typedoc/node_modules/typescript
./node_modules/typedoc/node_modules/typescript/lib/typescript.d.ts
./node_modules/typedoc/node_modules/typescript/lib/typescriptServices.d.ts
./node_modules/typedoc/node_modules/typescript/lib/typescript.js
./node_modules/typedoc/node_modules/typescript/lib/typescriptServices.js
./node_modules/typedoc/dist/lib/utils/options/sources/typescript.d.ts
./node_modules/typedoc/dist/lib/utils/options/sources/typescript.js
./node_modules/typedoc/dist/lib/utils/options/sources/typescript.js.map
./node_modules/typescript
./node_modules/typescript/lib/typescript.d.ts
./node_modules/typescript/lib/typescriptServices.d.ts
./node_modules/typescript/lib/typescript.js
./node_modules/typescript/lib/typescriptServices.js
```
