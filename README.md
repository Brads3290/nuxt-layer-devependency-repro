## Branch: `working`
Working example

The `working` branch is a working example of the layer having a runtime dependency (https://github.com/unjs/ufo) and working fine.
- `nuxt-layer` depends on, and uses, unjs/ufo
- Running `npm install` on `nuxt-app` installs `ufo` in `nuxt-app` (even though `nuxt-app` does not directly depend on it, but the layer does), and everything works.

## Branch: `repro`
Bug repro

The `repro` branch is an example of dev dependencies **NOT** following the same behaviour.
- `nuxt-layer` depends on, and uses, `@nuxt/tailwindcss` as a **dev dependency**
- Running `npm install` on `nuxt-app` fails.
- Adding the dev dependency to `nuxt-app` makes everything work again:

// package.json
```json
"devDependencies": {
    "@nuxtjs/tailwindcss": "^6.12.0"
},
```