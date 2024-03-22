# Minimal Reproduction of Error in Package with Drizzle Push

This repository contains a sample project that demonstrates how to reproduce an error when using `drizzle-kit push:[database]`

It is a minimal turborepo using their basic generator to create the packages.

* Clone the repo
* `pnpm i`
* `cd apps/web`
* `pnpm db:push`

error observed:

``` bash
Error [ERR_PACKAGE_PATH_NOT_EXPORTED]: No "exports" main defined in /Users/joel/Code/joelhooks/drizzle-fail-turbo/apps/web/node_modules/adapter-drizzle/package.json
    at __node_internal_captureLargerStackTrace (node:internal/errors:496:5)
    at new NodeError (node:internal/errors:405:5)
    at exportsNotFound (node:internal/modules/esm/resolve:261:10)
    at packageExportsResolve (node:internal/modules/esm/resolve:535:13)
    at resolveExports (node:internal/modules/cjs/loader:547:36)
    at Module._findPath (node:internal/modules/cjs/loader:621:31)
    at Module._resolveFilename (node:internal/modules/cjs/loader:1034:27)
    at Module._resolveFilename (/Users/joel/Code/joelhooks/drizzle-fail-turbo/node_modules/.pnpm/drizzle-kit@0.20.14/node_modules/drizzle-kit/bin.cjs:11140:40)
    at Module._load (node:internal/modules/cjs/loader:901:27)
    at Module.require (node:internal/modules/cjs/loader:1115:19)
    at require (node:internal/modules/helpers:130:18)
    at Object.<anonymous> (/Users/joel/Code/joelhooks/drizzle-fail-turbo/apps/web/db/schema.ts:1:21)
    at Module._compile (node:internal/modules/cjs/loader:1233:14)
    at Module._compile (/Users/joel/Code/joelhooks/drizzle-fail-turbo/node_modules/.pnpm/drizzle-kit@0.20.14/node_modules/drizzle-kit/bin.cjs:8644:30)
    at Module._extensions..js (node:internal/modules/cjs/loader:1287:10)
    at Object.newLoader [as .ts] (/Users/joel/Code/joelhooks/drizzle-fail-turbo/node_modules/.pnpm/drizzle-kit@0.20.14/node_modules/drizzle-kit/bin.cjs:8648:13)
    at Module.load (node:internal/modules/cjs/loader:1091:32)
    at Module._load (node:internal/modules/cjs/loader:938:12)
    at Module.require (node:internal/modules/cjs/loader:1115:19)
    at require (node:internal/modules/helpers:130:18)
    at prepareFromSqliteImports (/Users/joel/Code/joelhooks/drizzle-fail-turbo/node_modules/.pnpm/drizzle-kit@0.20.14/node_modules/drizzle-kit/bin.cjs:12840:20)
    at async serializeSQLite (/Users/joel/Code/joelhooks/drizzle-fail-turbo/node_modules/.pnpm/drizzle-kit@0.20.14/node_modules/drizzle-kit/bin.cjs:13317:33)
    at async prepareSQLiteDbPushSnapshot (/Users/joel/Code/joelhooks/drizzle-fail-turbo/node_modules/.pnpm/drizzle-kit@0.20.14/node_modules/drizzle-kit/bin.cjs:13366:26)
    at async prepareSQLitePush (/Users/joel/Code/joelhooks/drizzle-fail-turbo/node_modules/.pnpm/drizzle-kit@0.20.14/node_modules/drizzle-kit/bin.cjs:14878:31)
    at async Command.<anonymous> (/Users/joel/Code/joelhooks/drizzle-fail-turbo/node_modules/.pnpm/drizzle-kit@0.20.14/node_modules/drizzle-kit/bin.cjs:63296:22) {
  code: 'ERR_PACKAGE_PATH_NOT_EXPORTED'

```



