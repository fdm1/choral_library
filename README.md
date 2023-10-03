# Choral library

https://fdm1.github.io/choral_library

An attempt to create a static choral library site backed on GH pages.

The db will be a sqlite file in the repo, and the site will be built with SvelteKit.

Any CRUD actions will be done via GH actions in the repo, which will update the db file, and commit the changes to it. Alternatively, the db might live somewhere else (like dropbox?). Making this up as I go along

### Deploying to GH pages

```bash
yarn deploy
```

### Developing

```bash
yarn run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

#### References used to hack this together
- https://www.okupter.com/blog/deploy-sveltekit-website-to-github-pages
- https://github.com/JustinyAhin/sveltekit-github-pages


