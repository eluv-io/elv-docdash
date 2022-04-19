# elv-docdash

**This is a modified version of the [Docdash](docdashhttps://github.com/clenemt/docdash) JSDoc theme by [Clement Moron](https://github.com/clenemt).** See [CHANGELOG.md](./CHANGELOG.md) for a list of customizations.


## Install

```bash
$ npm install --save-dev @eluvio/elv-docdash
```

## Usage (npm)
In your projects `package.json` file add a new script:

```json
"script": {
  "generate-docs": "node_modules/.bin/jsdoc -c .jsdoc.json"
}
```

In your `.jsdoc.json` file, add an /opts/template option and a /docdash section:

## Sample `.jsdoc.json`

```json
{
  "tags": {
    "allowUnknownTags": true,
    "dictionaries": ["jsdoc"]
  },
  "source": {
    "include": ["src"],
    "includePattern": ".js$",
    "excludePattern": "(node_modules/|docs)"
  },
  "plugins": [
    "plugins/markdown"
  ],
  "opts": {
    "destination": "./docs/",
    "encoding": "utf8",
    "pedantic": true,
    "private": false,
    "recurse": true,
    "template": "node_modules/@eluvio/elv-docdash"
  },
  "docdash": {
    "static": true,
    "sort": true,
    "search": true,
    "collapse": true,
    "typedefs": true,
    "removeQuotes": "none",
    "scripts": [],
    "menu":{
      "Github repo": {
        "href":"HTTPS_LINK_TO_YOUR_GITHUB_REPO",
        "target":"_blank",
        "class":"menu-item",
        "id":"repository"
      }
    }
  }
}
```

## License
Licensed under the Apache License, version 2.0. (see [Apache-2.0](LICENSE.md)).
