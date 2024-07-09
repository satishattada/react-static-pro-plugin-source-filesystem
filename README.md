# react-static-pro-plugin-source-filesystem

A [React-Static-Pro] plugin that adds support for recursively importing routes from a directory

This means that any files in your projects `pages/` directory will be turned into static routes.

Example: 
- src/pages/index.js - would produce a route with the path of `/` and the template set to `src/pages/index.js`
- src/pages/about-us.js - would produce a route with the page of `/about-us` and the template set to `src/pages/about-us.js`

## Installation

In an existing react-static site run:

```bash
$ yarn add react-static-pro-plugin-source-filesystem
```

Then add the plugin to your `static.config.js` with a valid `location` directory in the options:

```javascript
...
import path from 'path'
...
export default {
  plugins: [
    [
      'react-static-pro-plugin-source-filesystem',
      {
        location: path.resolve('./src/pages'),
      },
    ],
  ],
}
```
