# Advanced CSS

All three projects use one package.json.

## Links:
- [Natours](https://css-projects.netlify.app/natours/)
- [Nexter](https://css-projects.netlify.app/nexter/)
- [Trillo](https://css-projects.netlify.app/trillo/)


### Scripts for Natours:

```
  "scripts": {
    "watch": "node-sass -wr Natours/sass/main.scss Natours/css/style.css",
    "compile": "node-sass Natours/sass/main.scss Natours/css/style.comp.css",
    "concat": "concat -o Natours/css/style.concat.css Natours/css/icon-font.css Natours/css/style.comp.css",
    "prefix": "postcss --use autoprefixer -b 'last 10 versions' Natours/css/style.concat.css -o Natours/css/style.prefix.css",
    "compress": "node-sass Natours/css/style.prefix.css Natours/css/style.css --output-style compressed",
    "build": "npm-run-all compile concat prefix compress"
  },
```

### Scripts for Trillo:

```
  "scripts": {
    "watch": "node-sass -wr Trillo/sass/main.scss Trillo/css/style.css",
    "compile": "node-sass Trillo/sass/main.scss Trillo/css/style.comp.css",
    "prefix": "postcss --use autoprefixer -b 'last 10 versions' Trillo/css/style.comp.css -o Trillo/css/style.prefix.css",
    "compress": "node-sass Trillo/css/style.prefix.css Trillo/css/style.css --output-style compressed",
    "build": "npm-run-all compile prefix compress"
  },
```

### Scripts for Nexter:

```
  "scripts": {
    "watch": "node-sass -wr Nexter/sass/main.scss Nexter/css/style.css",
    "compile": "node-sass Nexter/sass/main.scss Nexter/css/style.comp.css",
    "prefix": "postcss --use autoprefixer -b 'last 10 versions' Nexter/css/style.comp.css -o Nexter/css/style.prefix.css",
    "compress": "node-sass Nexter/css/style.prefix.css Nexter/css/style.css --output-style compressed",
    "build": "npm-run-all compile prefix compress"
  },
```
