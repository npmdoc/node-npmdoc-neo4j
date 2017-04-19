# npmdoc-neo4j

#### api documentation for  [neo4j (v1.1.1)](https://github.com/thingdom/node-neo4j)  [![npm package](https://img.shields.io/npm/v/npmdoc-neo4j.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-neo4j) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-neo4j.svg)](https://travis-ci.org/npmdoc/node-npmdoc-neo4j)

#### Neo4j driver (REST API client) for Node.js

[![NPM](https://nodei.co/npm/neo4j.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/neo4j)

- [https://npmdoc.github.io/node-npmdoc-neo4j/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-neo4j/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-neo4j/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-neo4j/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-neo4j/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-neo4j/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "The Thingdom"
    },
    "bugs": {
        "url": "https://github.com/thingdom/node-neo4j/issues"
    },
    "contributors": [
        {
            "name": "Daniel Gasienica"
        },
        {
            "name": "Aseem Kishore"
        },
        {
            "name": "Sergio Haro"
        }
    ],
    "dependencies": {
        "http-status": "^0.1.0",
        "request": "^2.27.0"
    },
    "description": "Neo4j driver (REST API client) for Node.js",
    "devDependencies": {
        "chai": "^1.8.0",
        "codo": "^1.5.0",
        "coffee-script": "1.7.x",
        "mocha": "^1.3.0",
        "streamline": "^0.10.16"
    },
    "directories": {},
    "dist": {
        "shasum": "5982f1aa11e7d6881e70616238cb05d6fdbb30cd",
        "tarball": "https://registry.npmjs.org/neo4j/-/neo4j-1.1.1.tgz"
    },
    "engines": {
        "node": ">= 0.6"
    },
    "homepage": "https://github.com/thingdom/node-neo4j",
    "keywords": [
        "neo4j",
        "graph",
        "database",
        "driver",
        "rest",
        "api",
        "client"
    ],
    "licenses": [
        {
            "type": "Apache License, Version 2.0",
            "url": "http://www.apache.org/licenses/LICENSE-2.0.html"
        }
    ],
    "main": "./lib",
    "maintainers": [
        {
            "name": "gasi"
        },
        {
            "name": "aseemk"
        }
    ],
    "name": "neo4j",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/thingdom/node-neo4j.git"
    },
    "scripts": {
        "build": "coffee -m -c lib/ && _coffee -m --standalone -c lib/",
        "clean": "rm -f lib/*.{js,map}",
        "codo": "codo && codo --server",
        "postpublish": "npm run clean",
        "prepublish": "npm run build",
        "test": "mocha"
    },
    "version": "1.1.1"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
