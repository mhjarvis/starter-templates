# Astro Setup

## Basic Setup

Setup new project by following cli instructions:

```sh
npm create astro@latest
```

To add React integration, we can run:

```sh
npx astro add react
```

## Folder Structure

- `src/pages` - Astro uses file-system page routing, meaning any files/folders placed in `/pages` will
  act as a route and can be linked to:

```html
<a href="/about"></a>
```

- `src/components` - store components (similar to React).

- `src/layouts` - should contain any files pertaining to UI structure.

- `src/styles` - stores css or sass files.

- `src/content` - used by content collections.

- `public/` - stores images and fonts.

- `astro.config.mjs` - file that allows us to specify Astro's behavior or add plugins.

## Astro File Anatomy

Astro files are made up of the component script (usually on top), seperated by a 'code fence' (`---`) before and after the script section. This is where JS or TS goes, you can import componets, etc. Code written here will never make it to the client.

The second part of the component is the template. This is where html will be placed. Example:

```js
---
const name = 'Jack'
---
<h1>Hello there, {name}</h1>
```

\*\* NOTE - JavaScript code placed between the fence will executes during build time while code placed in the template section will be executes at the request time. This might be important when considering time-based code.

### Styling

CSS is scoped to the component where it is defined. Global styles can be created by adding the `is:global` attribute:

```html
<style is:global>
	p {
		font-weight: bold;
	}
</style>
```

CSS variables can also be used from the script part of an Astro file:

```js
---
const important = `#f00`;
---
<style define:vars={{ important }}>
p {
  color: var(--important);
}
</style>
<p>Important message</p>
```

Stylesheets placed in the public folder can also be imported:

```js
---
import '../path/to/style.css'
---
<p>some html...</p>
```
