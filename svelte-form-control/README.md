# Svelte Form Control

[Live Demo](svelte-form-control.surge.sh)

- https://material-ui.com/
- https://sveltematerialui.com/
- https://kamyarlajani.medium.com/svelte-form-validation-using-yup-7d4cd5985849
- https://github.com/KamyarLajani/svelte-yup
## Requirements

- NodeJshttps://github.com/KamyarLajani/svelte-yup
- [Rollup](https://rollupjs.org):

## Run the app

In Development
```bash
    npm i
    npm run dev
```

In Production

```bash
    npm run build
```



You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).


## Single-page app mode

By default, sirv will only respond to requests that match files in `public`. This is to maximise compatibility with static fileservers, allowing you to deploy your app anywhere.

If you're building a single-page app (SPA) with multiple routes, sirv needs to be able to respond to requests for *any* path. You can make it so by editing the `"start"` command in package.json:

```js
"start": "sirv public --single"
```

### Deployed with [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
    npm install -g surge
```

Then, from within your project folder:

```bash
    npm run build
    surge public svelte-form-control.surge.sh
```
