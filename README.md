# 11ty-global-data

Testing global site information in the _data directory.

This repo shows how you can get data from a global data file in your project's `_data/` directory and use it in your templates.

```sh
tree
.
├── package-lock.json
├── package.json
│
├── site/ # INPUT DIR
│   ├── _data/
│   │   └── site.json
│   └── pages/
│       └── index.njk
│
└── www/ # OUTPUT DIR
    └── index.html

4 directories, 5 files
```

If you wanted to use dynamic data in your global `site` data file, you could rename the `site/_data/site.json` file to `site/_data/site.js` and use JavaScript and

```js
// ./site/_data/site.js
module.exports = {
  author: "Peter deHaan",
  github: "pdehaan",
  twitter: "pdehaan",
  license: "MPL-2.0"
};
```

Or even return an async function, if you wanted to do any async data fetching/processing:

```js
// ./site/_data/site.js
module.exports = async () => {
  return {
    author: "Peter deHaan",
    github: "pdehaan",
    twitter: "pdehaan",
    license: "MPL-2.0"
  };
};
```
