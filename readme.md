# webpack-base

This is the base StackBlitz project for other webpack-related demos.
It has `webpack`, `webpack-cli` and `http-server` installed.

You can also debug webpack in the browser, I made a video about it [here](https://www.youtube.com/watch?v=9s-t3uECOic&t=2s).

## Setting up

The problem I'm facing at the time of writing is that StackBlitz hides the `src/node_modules` folder and does not preseve it across page refreshes.

So, a temporary solution to this was to manually do the below steps, since the files' content is little.

First, we create the folder and its constituent files:

```bash
# Make sure you're running this command from the root of this workspace.
mkdir src/node_modules/ && cd src/node_modules/ && touch x.js && touch y.js && touch z.js
```

Then, we make the files visible in the left panel:

```bash
# Make sure you're in the `src/node_modules` directory.
code x.js && code y.js && code z.js
```

Now, we just add the following content(`echo "foo" >> file.js` doesn't seem to work):

```js
// x.js
export default 'some content from `x.js`!';
```

```js
// y.js
export default 'y';
```

```js
// z.js
export default 'z';
```

Eventually, you might want to `cd` back into the root of this workspace:

```bash
cd -
```

---

## Running webpack

```bash
npm run build
```

---

## Opening in the browser

By default, it looks into the `./dist` directory.

```bash
npm start
```
