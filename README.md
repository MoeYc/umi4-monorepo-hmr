# umi4-monorepo-hmr

### 1. Add `monorepoRedirect` to project config file

See [`.umirc.ts`](./packages/app/.umirc.ts)

```ts
// .umirc.ts

export default {
  monorepoRedirect: {},
}
```

### 2. Directory Structure

```bash
./packages
└── lib
    └── src
```

`monorepoRedirect` can auto alias to `src/index` for typescript transpiler and HMR.

use `srcDir` change alias dest position:

```ts
// .umirc.ts

export default {
  monorepoRedirect: {
    // first alias to `lib/index`, if 'lib' does not exist, alias to 'src/index'
    srcDir: ['./lib', './src']
  },
}
```
