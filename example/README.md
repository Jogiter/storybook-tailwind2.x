# storybook-tailwind

this demo using postcss7.x

## steps

1. add `@storybook/addon-postcss`

```js
// main.js
addons: [
  '@storybook/addon-postcss',
],
```

2. tailwindcss install

> [tailwindcss#post-css-7-compatibility-build](https://tailwindcss.com/docs/installation#post-css-7-compatibility-build)

```sh
npm uninstall tailwindcss postcss autoprefixer
npm install tailwindcss@npm:@tailwindcss/postcss7-compat @tailwindcss/postcss7-compat postcss@^7 autoprefixer@^9
```

3. setup tailwind-config

```sh
npx tailwindcss init
```

4. create `tailwind.css`

```css
/* tailwind.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

5. add `.storybook/postcss.config.js`

```js
module.exports = require('../postcss.config');
```

6. add tailwind.css to `preview.js`

```js
import '../tailwind.css';
```

## run

```sh
# dev
yarn storybook

# build
yarn build-storybook
```
