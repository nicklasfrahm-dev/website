# Personal Website

This repository contains the code for my personal website. It is built using [SvelteKit][svelte-kit] and [Flowbite Svelte][flowbite-svelte]. I am using [GitHub Pages][github-pages] to host it.

## Developing

Make sure to have a recent LTS of [Node][node] installed. We recommend using [nvm][nvm] to manage Node versions.

```bash
# Install dependencies.
npm ci
# Start the development server.
npm run dev
# Start the server and open the app in a new browser tab.
npm run dev -- --open
```

## Building

To create a production version of the app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

[node]: https://nodejs.org/
[nvm]: https://github.com/nvm-sh/nvm
[svelte-kit]: https://kit.svelte.dev/
[flowbite-svelte]: https://flowbite.com/svelte
[github-pages]: https://pages.github.com/
