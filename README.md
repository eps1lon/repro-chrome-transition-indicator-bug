#

## Steps to reproduce

```console
$ pnpm install --frozen-lockfile
$ pnpm next dev
```

Then open http://localhost:3000 in "Chrome for testing".
I used [136.0.7103.113 Mac ARM](https://storage.googleapis.com/chrome-for-testing-public/136.0.7103.113/mac-arm64/chrome-mac-arm64.zip).

## Actual behavior

Page crashes on landing first. Repeated visits do not crash.
The dev server and! browser need to be restarted to reproduce the crash again.

When you comment out [./node_modules/next/dist/client/app-index.js#66](./node_modules/next/dist/client/app-index.js#66) and restart the dev server, no crash occurs.

## Expected behavior

No crash ever
