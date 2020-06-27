# Advanced CSS

All three projects use one package.json.

### Scripts for Natours:

```
  "scripts": {
    "watch": "node-sass -wr Natours/starter/sass/main.scss Natours/starter/css/style.css",
    "compile": "node-sass Natours/starter/sass/main.scss Natours/starter/css/style.comp.css",
    "concat": "concat -o Natours/starter/css/style.concat.css Natours/starter/css/icon-font.css Natours/starter/css/style.comp.css",
    "prefix": "postcss --use autoprefixer -b 'last 10 versions' Natours/starter/css/style.concat.css -o Natours/starter/css/style.prefix.css",
    "compress": "node-sass Natours/starter/css/style.prefix.css Natours/starter/css/style.css --output-style compressed",
    "build": "npm-run-all compile concat prefix compress"
  },
```

### Scripts for Trillo:

```
  "scripts": {
    "watch": "node-sass -wr Trillo/starter/sass/main.scss Trillo/starter/css/style.css",
    "compile": "node-sass Trillo/starter/sass/main.scss Trillo/starter/css/style.comp.css",
    "prefix": "postcss --use autoprefixer -b 'last 10 versions' Trillo/starter/css/style.comp.css -o Trillo/starter/css/style.prefix.css",
    "compress": "node-sass Trillo/starter/css/style.prefix.css Trillo/starter/css/style.css --output-style compressed",
    "build": "npm-run-all compile prefix compress"
  },
```
