# vanilla-template [![downloads](https://badgen.now.sh/npm/dm/@pota/vanilla-template)](https://npmjs.org/package/@pota/vanilla-template)

## Setup 🚀

You can create a new project using [`create-pota`](../../core/create-pota).

```bash
npx pota --template vanilla
```

<!--
During project creation, everything above this comment should _ideally_ be replaced with a `Quick Start` on how to run & build the project, referencing the project title in the heading, instead of the skeleton's.
-->

## Standards 📒

This project follows the
[MediaMonks Frontend Coding Standards](https://github.com/mediamonks/frontend-coding-standards)

## Features 🔋

### Pota Scripts [TODO]

<br />

_hidden TODOs_

<!--
- TODO: describe how to set defaults for these options in `.pota/commands/{command}.js`
- TODO: describe how to create new commands (possible link to `@pota/cli` docs)
-->

<hr />
skeleton
| Script            | Description                                                                |
| ----------------- | -------------------------------------------------------------------------- |
| **`typecheck`**   | Checks for type errors and unused variables/types in the source directory. |
| **`fix`**         | Executes all `fix:*` and `format commands in sequence.                     |
| **`fix:eslint`**  | Executes `eslint:lint` and fixes fixable errors.                           |
| **`format`**      | Formats the source files using `prettier`.                                 |
| **`lint`**        | Executes all `lint:*` commands in sequence.                                |
| **`lint:eslint`** | Lints the source files using `eslint`.                                     |
| **`rsync`**       | Synchronizes (uploads) `dist/` files to a remote server.                   |

<hr />

### JavaScript / TypeScript

_hidden TODOs_

<!--
- TODO: describe `ts-loader` usage how `ts-loader` and `babel` transpile TS and
- TODO: describe `babel` usage and it plugins
- TODO: describe what ES version is the output and how to control it (`browserslist`)
- TODO: describe where polyfills go
-->

<hr />

### CSS

_hidden TODOs_

<!--
- TODO: CSS Modules
- TODO: SCSS
- TODO: PostCSS
- TODO: Modernizr?
- TODO: normalize.css?
-->

<hr />

### Images

_hidden TODOs_

<!--
- TODO: describe how we handle SVGs (e.g. `file.svg` vs `file.svg?raw`)
- TODO: describe how we compress image files and how to configure it
-->

<hr />

### Misc. Assets

_hidden TODOs_

<!--
- TODO: describe what other assets the skeleton supports
-->

<hr />

### Linting & Formatting

_hidden TODOs_

<!--
- TODO: describe how `eslint` is included and how to configure it
- TODO: describe how `prettier` is included and how to configure it
-->

<hr />

### Service Worker

The skeleton has opt-in support for
[service workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API/Using_Service_Workers)
through the help of [workbox](https://developers.google.com/web/tools/workbox/).

To get started, you can create `/src/service-worker.ts` file to customize workbox and its many
[modules](https://developers.google.com/web/tools/workbox/modules) .

> This is how an example service worker file could look like:

```ts
/// <reference lib="webworker" />

import { clientsClaim } from 'workbox-core';
import { precacheAndRoute } from 'workbox-precaching';

declare const self: ServiceWorkerGlobalScope;

clientsClaim();

// eslint-disable-next-line no-underscore-dangle
precacheAndRoute(self.__WB_MANIFEST);
```

Now, whenever you bundle your application for production, a `service-worker.js` file will be
generated.

As a last step, you need to make sure to register the service worker using the
`serviceWorkerRegistration.ts` module, see the comment in `main.ts` for more details.

### Deployment

#### Remote Sync

For simple deployments, when you just want to upload your files to a remote server, you can use the
`rsync` script.

Note: before using the `rsync` script, make sure to configure a host in in the "package.json"

```bash
npm pkg set config.host="github.com"
```

_hidden TODOs_

<!--
- TODO: describe how `rsync` and the associated `upload-build` script works and how to configure it
-->

<hr />

### Git

_hidden TODOs_

<!--
- TODO: describe `lint-staged` and `husky?`
- TODO: describe how we extract ticket identifiers from branch names
-->

<hr />

### Continuous Integration / Continuous Deployment

#### Bitbucket

`webpack-skeleton` comes with `bitbucket-pipelines.yml`, pre-configured to run `check-types`, `lint`
and `test` scripts.

_hidden TODOs_

<!--
- TODO: describe how to use parallelization
- TODO: describe how to setup deploys with `rsync`
-->
