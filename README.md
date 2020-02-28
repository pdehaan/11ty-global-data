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