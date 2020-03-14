# use-http-202
Reproduces [use-http issue #202](https://github.com/alex-cory/use-http/issues/202).

1. Install yarn (I used version 1.22.1)
2. Run:

       yarn install
       yarn start

## Expected behavior
No warnings logged during the build.

## Actual behavior
The following warnings are logged during the build:

```
⚠️  Could not load source file "../src/index.ts" in source map of "node_modules/use-http/dist/index.js".
⚠️  Could not load source file "../src/useFetch.ts" in source map of "node_modules/use-http/dist/useFetch.js".
⚠️  Could not load source file "../src/useMutation.ts" in source map of "node_modules/use-http/dist/useMutation.js".
⚠️  Could not load source file "../src/useQuery.ts" in source map of "node_modules/use-http/dist/useQuery.js".
⚠️  Could not load source file "../src/Provider.tsx" in source map of "node_modules/use-http/dist/Provider.js".
⚠️  Could not load source file "../src/FetchContext.ts" in source map of "node_modules/use-http/dist/FetchContext.js".
⚠️  Could not load source file "../src/types.ts" in source map of "node_modules/use-http/dist/types.js".
⚠️  Could not load source file "../src/utils.ts" in source map of "node_modules/use-http/dist/utils.js".
⚠️  Could not load source file "../src/useFetchArgs.ts" in source map of "node_modules/use-http/dist/useFetchArgs.js".
⚠️  Could not load source file "../src/doFetchArgs.ts" in source map of "node_modules/use-http/dist/doFetchArgs.js".
⚠️  Could not load source file "../useSSR.ts" in source map of "node_modules/use-ssr/dist/useSSR.js".
⚠️  Could not load source file "../src/index.ts" in source map of "node_modules/use-http/dist/index.js".
⚠️  Could not load source file "../src/useFetch.ts" in source map of "node_modules/use-http/dist/useFetch.js".
⚠️  Could not load source file "../src/useMutation.ts" in source map of "node_modules/use-http/dist/useMutation.js".
⚠️  Could not load source file "../src/useQuery.ts" in source map of "node_modules/use-http/dist/useQuery.js".
⚠️  Could not load source file "../src/Provider.tsx" in source map of "node_modules/use-http/dist/Provider.js".
⚠️  Could not load source file "../useSSR.ts" in source map of "node_modules/use-ssr/dist/useSSR.js".
⚠️  Could not load source file "../src/FetchContext.ts" in source map of "node_modules/use-http/dist/FetchContext.js".
⚠️  Could not load source file "../src/types.ts" in source map of "node_modules/use-http/dist/types.js".
⚠️  Could not load source file "../src/utils.ts" in source map of "node_modules/use-http/dist/utils.js".
⚠️  Could not load source file "../src/useFetchArgs.ts" in source map of "node_modules/use-http/dist/useFetchArgs.js".
⚠️  Could not load source file "../src/doFetchArgs.ts" in source map of "node_modules/use-http/dist/doFetchArgs.js".
```

The problem seems to be that the sourcemaps shipped by use-http refer to .ts files 
that don't exist in the distribution.
