# api documentation for  [neo4j (v1.1.1)](https://github.com/thingdom/node-neo4j)  [![npm package](https://img.shields.io/npm/v/npmdoc-neo4j.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-neo4j) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-neo4j.svg)](https://travis-ci.org/npmdoc/node-npmdoc-neo4j)
#### Neo4j driver (REST API client) for Node.js

[![NPM](https://nodei.co/npm/neo4j.png?downloads=true)](https://www.npmjs.com/package/neo4j)

[![apidoc](https://npmdoc.github.io/node-npmdoc-neo4j/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-neo4j_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-neo4j/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-neo4j/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-neo4j/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "The Thingdom",
        "email": "info@thethingdom.com"
    },
    "bugs": {
        "url": "https://github.com/thingdom/node-neo4j/issues"
    },
    "contributors": [
        {
            "name": "Daniel Gasienica",
            "email": "daniel@gasienica.ch"
        },
        {
            "name": "Aseem Kishore",
            "email": "aseem.kishore@gmail.com"
        },
        {
            "name": "Sergio Haro",
            "email": "sergio.haro.jr@gmail.com"
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
            "name": "gasi",
            "email": "daniel@gasienica.ch"
        },
        {
            "name": "aseemk",
            "email": "aseem.kishore@gmail.com"
        }
    ],
    "name": "neo4j",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module neo4j](#apidoc.module.neo4j)
1.  [function <span class="apidocSignatureSpan">neo4j.</span>GraphDatabase (opts)](#apidoc.element.neo4j.GraphDatabase)
1.  [function <span class="apidocSignatureSpan">neo4j.</span>Node (db, data)](#apidoc.element.neo4j.Node)
1.  [function <span class="apidocSignatureSpan">neo4j.</span>PropertyContainer (db, data)](#apidoc.element.neo4j.PropertyContainer)
1.  [function <span class="apidocSignatureSpan">neo4j.</span>Relationship (db, data, start, end)](#apidoc.element.neo4j.Relationship)
1.  [function <span class="apidocSignatureSpan">neo4j.</span>deserialize (o, separator)](#apidoc.element.neo4j.deserialize)
1.  [function <span class="apidocSignatureSpan">neo4j.</span>serialize (o, separator)](#apidoc.element.neo4j.serialize)
1.  object <span class="apidocSignatureSpan">neo4j.</span>GraphDatabase.prototype
1.  object <span class="apidocSignatureSpan">neo4j.</span>Node.prototype
1.  object <span class="apidocSignatureSpan">neo4j.</span>PropertyContainer.prototype
1.  object <span class="apidocSignatureSpan">neo4j.</span>Relationship.prototype
1.  object <span class="apidocSignatureSpan">neo4j.</span>util

#### [module neo4j.GraphDatabase](#apidoc.module.neo4j.GraphDatabase)
1.  [function <span class="apidocSignatureSpan">neo4j.</span>GraphDatabase (opts)](#apidoc.element.neo4j.GraphDatabase.GraphDatabase)

#### [module neo4j.GraphDatabase.prototype](#apidoc.module.neo4j.GraphDatabase.prototype)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>_getRoot (_)](#apidoc.element.neo4j.GraphDatabase.prototype._getRoot)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>_purgeCache ()](#apidoc.element.neo4j.GraphDatabase.prototype._purgeCache)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>_toJSON (obj)](#apidoc.element.neo4j.GraphDatabase.prototype._toJSON)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>createNode (data)](#apidoc.element.neo4j.GraphDatabase.prototype.createNode)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>createNodeIndex (name, config, callback)](#apidoc.element.neo4j.GraphDatabase.prototype.createNodeIndex)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>createRelationship (startNode, endNode, type, _)](#apidoc.element.neo4j.GraphDatabase.prototype.createRelationship)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>createRelationshipIndex (name, config, callback)](#apidoc.element.neo4j.GraphDatabase.prototype.createRelationshipIndex)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>deleteNodeIndex (name, _)](#apidoc.element.neo4j.GraphDatabase.prototype.deleteNodeIndex)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>deleteRelationshipIndex (name, _)](#apidoc.element.neo4j.GraphDatabase.prototype.deleteRelationshipIndex)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>execute (script, params, callback)](#apidoc.element.neo4j.GraphDatabase.prototype.execute)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>fromJSON (obj)](#apidoc.element.neo4j.GraphDatabase.prototype.fromJSON)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getIndexedNode (index, property, value, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getIndexedNode)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getIndexedNodes (index, property, value, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getIndexedNodes)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getIndexedRelationship (index, property, value, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getIndexedRelationship)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getIndexedRelationships (index, property, value, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getIndexedRelationships)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getNode (url, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getNode)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getNodeById (id, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getNodeById)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getNodeIndexes (_)](#apidoc.element.neo4j.GraphDatabase.prototype.getNodeIndexes)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getRelationship (url, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getRelationship)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getRelationshipById (id, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getRelationshipById)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getRelationshipIndexes (_)](#apidoc.element.neo4j.GraphDatabase.prototype.getRelationshipIndexes)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getServices (_)](#apidoc.element.neo4j.GraphDatabase.prototype.getServices)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>query (query, params, callback)](#apidoc.element.neo4j.GraphDatabase.prototype.query)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>queryNodeIndex (index, query, _)](#apidoc.element.neo4j.GraphDatabase.prototype.queryNodeIndex)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>queryRelationshipIndex (index, query, _)](#apidoc.element.neo4j.GraphDatabase.prototype.queryRelationshipIndex)
1.  [function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>reviveJSON (key, val)](#apidoc.element.neo4j.GraphDatabase.prototype.reviveJSON)

#### [module neo4j.Node](#apidoc.module.neo4j.Node)
1.  [function <span class="apidocSignatureSpan">neo4j.</span>Node (db, data)](#apidoc.element.neo4j.Node.Node)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.</span>_fromJSON (db, obj)](#apidoc.element.neo4j.Node._fromJSON)
1.  object <span class="apidocSignatureSpan">neo4j.Node.</span>__super__

#### [module neo4j.Node.prototype](#apidoc.module.neo4j.Node.prototype)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>_createRelationship (from, to, type, data, _)](#apidoc.element.neo4j.Node.prototype._createRelationship)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>_getRelationships (direction, type, _)](#apidoc.element.neo4j.Node.prototype._getRelationships)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>all (type, _)](#apidoc.element.neo4j.Node.prototype.all)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>constructor (db, data)](#apidoc.element.neo4j.Node.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>createRelationshipFrom (otherNode, type, data, cb)](#apidoc.element.neo4j.Node.prototype.createRelationshipFrom)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>createRelationshipTo (otherNode, type, data, cb)](#apidoc.element.neo4j.Node.prototype.createRelationshipTo)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>delete (_, force)](#apidoc.element.neo4j.Node.prototype.delete)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>getRelationshipNodes (rels, _)](#apidoc.element.neo4j.Node.prototype.getRelationshipNodes)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>getRelationships (type, _)](#apidoc.element.neo4j.Node.prototype.getRelationships)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>incoming (type, _)](#apidoc.element.neo4j.Node.prototype.incoming)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>index (index, key, value, _)](#apidoc.element.neo4j.Node.prototype.index)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>outgoing (type, _)](#apidoc.element.neo4j.Node.prototype.outgoing)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>path (to, type, direction, maxDepth, algorithm, _)](#apidoc.element.neo4j.Node.prototype.path)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>save (_)](#apidoc.element.neo4j.Node.prototype.save)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>toString ()](#apidoc.element.neo4j.Node.prototype.toString)
1.  [function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>unindex (index, key, value, callback)](#apidoc.element.neo4j.Node.prototype.unindex)

#### [module neo4j.PropertyContainer](#apidoc.module.neo4j.PropertyContainer)
1.  [function <span class="apidocSignatureSpan">neo4j.</span>PropertyContainer (db, data)](#apidoc.element.neo4j.PropertyContainer.PropertyContainer)
1.  [function <span class="apidocSignatureSpan">neo4j.PropertyContainer.</span>_fromJSON (db, obj)](#apidoc.element.neo4j.PropertyContainer._fromJSON)

#### [module neo4j.PropertyContainer.prototype](#apidoc.module.neo4j.PropertyContainer.prototype)
1.  [function <span class="apidocSignatureSpan">neo4j.PropertyContainer.prototype.</span>del ()](#apidoc.element.neo4j.PropertyContainer.prototype.del)
1.  [function <span class="apidocSignatureSpan">neo4j.PropertyContainer.prototype.</span>delete (_)](#apidoc.element.neo4j.PropertyContainer.prototype.delete)
1.  [function <span class="apidocSignatureSpan">neo4j.PropertyContainer.prototype.</span>equals (other)](#apidoc.element.neo4j.PropertyContainer.prototype.equals)
1.  [function <span class="apidocSignatureSpan">neo4j.PropertyContainer.prototype.</span>toJSON ()](#apidoc.element.neo4j.PropertyContainer.prototype.toJSON)

#### [module neo4j.Relationship](#apidoc.module.neo4j.Relationship)
1.  [function <span class="apidocSignatureSpan">neo4j.</span>Relationship (db, data, start, end)](#apidoc.element.neo4j.Relationship.Relationship)
1.  [function <span class="apidocSignatureSpan">neo4j.Relationship.</span>_fromJSON (db, obj)](#apidoc.element.neo4j.Relationship._fromJSON)
1.  object <span class="apidocSignatureSpan">neo4j.Relationship.</span>__super__

#### [module neo4j.Relationship.prototype](#apidoc.module.neo4j.Relationship.prototype)
1.  [function <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>constructor (db, data, start, end)](#apidoc.element.neo4j.Relationship.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>index (index, key, value, _)](#apidoc.element.neo4j.Relationship.prototype.index)
1.  [function <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>save (_)](#apidoc.element.neo4j.Relationship.prototype.save)
1.  [function <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>toString ()](#apidoc.element.neo4j.Relationship.prototype.toString)
1.  [function <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>unindex (index, key, value, callback)](#apidoc.element.neo4j.Relationship.prototype.unindex)
1.  object <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>end
1.  object <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>start

#### [module neo4j.util](#apidoc.module.neo4j.util)
1.  [function <span class="apidocSignatureSpan">neo4j.util.</span>adjustError (error)](#apidoc.element.neo4j.util.adjustError)
1.  [function <span class="apidocSignatureSpan">neo4j.util.</span>deserialize (o, separator)](#apidoc.element.neo4j.util.deserialize)
1.  [function <span class="apidocSignatureSpan">neo4j.util.</span>serialize (o, separator)](#apidoc.element.neo4j.util.serialize)
1.  [function <span class="apidocSignatureSpan">neo4j.util.</span>transform (val, db)](#apidoc.element.neo4j.util.transform)
1.  [function <span class="apidocSignatureSpan">neo4j.util.</span>wrapRequest (_arg)](#apidoc.element.neo4j.util.wrapRequest)



# <a name="apidoc.module.neo4j"></a>[module neo4j](#apidoc.module.neo4j)

#### <a name="apidoc.element.neo4j.GraphDatabase"></a>[function <span class="apidocSignatureSpan">neo4j.</span>GraphDatabase (opts)](#apidoc.element.neo4j.GraphDatabase)
- description and source-code
```javascript
function GraphDatabase(opts) {
  this.reviveJSON = __bind(this.reviveJSON, this);
  opts = ((typeof opts === "string") ? {
    url: opts
  } : opts);
  this.url = opts.url;
  this._request = util.wrapRequest(opts);
  this._root = null;
  this._services = null;
}
```
- example usage
```shell
...
## Usage

To start, create a new instance of the 'GraphDatabase' class pointing to your
Neo4j instance:

'''js
var neo4j = require('neo4j');
var db = new neo4j.GraphDatabase('http://localhost:7474');
'''

Node.js is asynchronous, which means this library is too: most functions take
callbacks and return immediately, with the callbacks being invoked when the
corresponding HTTP requests and responses finish.

Here's a simple example:
...
```

#### <a name="apidoc.element.neo4j.Node"></a>[function <span class="apidocSignatureSpan">neo4j.</span>Node (db, data)](#apidoc.element.neo4j.Node)
- description and source-code
```javascript
function Node(db, data) {
  Node.__super__.constructor.call(this, db, data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.PropertyContainer"></a>[function <span class="apidocSignatureSpan">neo4j.</span>PropertyContainer (db, data)](#apidoc.element.neo4j.PropertyContainer)
- description and source-code
```javascript
function PropertyContainer(db, data) {
  this.db = db;
  this._request = db._request;
  this._data = (data || {
  });
  this._data.self = ((((data != null) ? data.self : void 0)) || null);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Relationship"></a>[function <span class="apidocSignatureSpan">neo4j.</span>Relationship (db, data, start, end)](#apidoc.element.neo4j.Relationship)
- description and source-code
```javascript
function Relationship(db, data, start, end) {
  var Node;
  Relationship.__super__.constructor.call(this, db, data);
  Node = require("./Node");
  this._start = (start || new Node(db, {
    self: data.start
  }));
  this._end = (end || new Node(db, {
    self: data.end
  }));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.deserialize"></a>[function <span class="apidocSignatureSpan">neo4j.</span>deserialize (o, separator)](#apidoc.element.neo4j.deserialize)
- description and source-code
```javascript
deserialize = function (o, separator) {
  return unflatten(JSON.parse(o), separator);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.serialize"></a>[function <span class="apidocSignatureSpan">neo4j.</span>serialize (o, separator)](#apidoc.element.neo4j.serialize)
- description and source-code
```javascript
serialize = function (o, separator) {
  return JSON.stringify(flatten(o, separator));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.neo4j.GraphDatabase"></a>[module neo4j.GraphDatabase](#apidoc.module.neo4j.GraphDatabase)

#### <a name="apidoc.element.neo4j.GraphDatabase.GraphDatabase"></a>[function <span class="apidocSignatureSpan">neo4j.</span>GraphDatabase (opts)](#apidoc.element.neo4j.GraphDatabase.GraphDatabase)
- description and source-code
```javascript
function GraphDatabase(opts) {
  this.reviveJSON = __bind(this.reviveJSON, this);
  opts = ((typeof opts === "string") ? {
    url: opts
  } : opts);
  this.url = opts.url;
  this._request = util.wrapRequest(opts);
  this._root = null;
  this._services = null;
}
```
- example usage
```shell
...
## Usage

To start, create a new instance of the 'GraphDatabase' class pointing to your
Neo4j instance:

'''js
var neo4j = require('neo4j');
var db = new neo4j.GraphDatabase('http://localhost:7474');
'''

Node.js is asynchronous, which means this library is too: most functions take
callbacks and return immediately, with the callbacks being invoked when the
corresponding HTTP requests and responses finish.

Here's a simple example:
...
```



# <a name="apidoc.module.neo4j.GraphDatabase.prototype"></a>[module neo4j.GraphDatabase.prototype](#apidoc.module.neo4j.GraphDatabase.prototype)

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype._getRoot"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>_getRoot (_)](#apidoc.element.neo4j.GraphDatabase.prototype._getRoot)
- description and source-code
```javascript
function GraphDatabase_prototype__getRoot__1(_) {
  var error, response, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype__getRoot__1",
    line: 76
  };
  return __func(_, this, arguments, GraphDatabase_prototype__getRoot__1, 0, __frame, function __$GraphDatabase_prototype__getRoot__1
() {
    if ((__this._root != null)) {
      return _(null, __this._root);
    }
    ;
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype__getRoot__1() {
          return __this._request.get(__this.url, __cb(_, __frame, 5, 33, function ___(__0, __1) {
            response = __1;
            if ((response.statusCode !== status.OK)) {
              return _(response);
            }
            ;
            return _(null, __this._root = response.body);
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype__getRoot__1() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype__getRoot__1() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype._purgeCache"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>_purgeCache ()](#apidoc.element.neo4j.GraphDatabase.prototype._purgeCache)
- description and source-code
```javascript
_purgeCache = function () {
  this._root = null;
  return this._services = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype._toJSON"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>_toJSON (obj)](#apidoc.element.neo4j.GraphDatabase.prototype._toJSON)
- description and source-code
```javascript
_toJSON = function (obj) {
  var json;
  json = {
  };
  json[JSON_KEY] = {
    version: PACKAGE.version,
    constructor: obj.constructor.name
  };
  return json;
}
```
- example usage
```shell
...
  });
};
PropertyContainer.prototype.del = function() {
  return this["delete"].apply(this, arguments);
};
PropertyContainer.prototype.toJSON = function() {
  var json;
  json = this.db._toJSON(this);
  json._data = this._data;
  return json;
};
PropertyContainer._fromJSON = function(db, obj) {
  var _data;
  _data = obj._data;
  return new this(db, _data);
...
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.createNode"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>createNode (data)](#apidoc.element.neo4j.GraphDatabase.prototype.createNode)
- description and source-code
```javascript
createNode = function (data) {
  var node;
  data = (data || {
  });
  node = new Node(this, {
    data: data
  });
  return node;
}
```
- example usage
```shell
...
Node.js is asynchronous, which means this library is too: most functions take
callbacks and return immediately, with the callbacks being invoked when the
corresponding HTTP requests and responses finish.

Here's a simple example:

'''js
var node = db.createNode({hello: 'world'});     // instantaneous, but...
node.save(function (err, node) {    // ...this is what actually persists.
    if (err) {
        console.error('Error saving new node to database:', err);
    } else {
        console.log('Node saved to database with id:', node.id);
    }
});
...
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.createNodeIndex"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>createNodeIndex (name, config, callback)](#apidoc.element.neo4j.GraphDatabase.prototype.createNodeIndex)
- description and source-code
```javascript
createNodeIndex = function (name, config, callback) {
  if ((typeof config === "function")) {
    callback = config;
    config = null;
  }
  ;
  return actual.call(this, name, config, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.createRelationship"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>createRelationship (startNode, endNode, type, _)](#apidoc.element.neo4j.GraphDatabase.prototype.createRelationship)
- description and source-code
```javascript
function GraphDatabase_prototype_createRelationship__8(startNode, endNode, type, _) {
  var __frame = {
    name: "GraphDatabase_prototype_createRelationship__8",
    line: 44
  };
  return __func(_, this, arguments, GraphDatabase_prototype_createRelationship__8, 3, __frame, function __$GraphDatabase_prototype_createRelationship__8
() {
    _();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.createRelationshipIndex"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>createRelationshipIndex (name, config, callback)](#apidoc.element.neo4j.GraphDatabase.prototype.createRelationshipIndex)
- description and source-code
```javascript
createRelationshipIndex = function (name, config, callback) {
  if ((typeof config === "function")) {
    callback = config;
    config = null;
  }
  ;
  return actual.call(this, name, config, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.deleteNodeIndex"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>deleteNodeIndex (name, _)](#apidoc.element.neo4j.GraphDatabase.prototype.deleteNodeIndex)
- description and source-code
```javascript
function GraphDatabase_prototype_deleteNodeIndex__16(name, _) {
  var error, response, services, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_deleteNodeIndex__16",
    line: 501
  };
  return __func(_, this, arguments, GraphDatabase_prototype_deleteNodeIndex__16, 1, __frame, function __$GraphDatabase_prototype_deleteNodeIndex__16
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_deleteNodeIndex__16() {
          return __this.getServices(__cb(_, __frame, 2, 24, function ___(__0, __1) {
            services = __1;
            return __this._request.del({
              url: ((("" + services.node_index) + "/") + (encodeURIComponent(name)))
            }, __cb(_, __frame, 3, 33, function ___(__0, __2) {
              response = __2;
              if ((response.statusCode !== status.NO_CONTENT)) {
                return _(response);
              }
              ;
              __then();
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_deleteNodeIndex__16() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_deleteNodeIndex__16() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.deleteRelationshipIndex"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>deleteRelationshipIndex (name, _)](#apidoc.element.neo4j.GraphDatabase.prototype.deleteRelationshipIndex)
- description and source-code
```javascript
function GraphDatabase_prototype_deleteRelationshipIndex__19(name, _) {
  var error, response, services, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_deleteRelationshipIndex__19",
    line: 594
  };
  return __func(_, this, arguments, GraphDatabase_prototype_deleteRelationshipIndex__19, 1, __frame, function __$GraphDatabase_prototype_deleteRelationshipIndex__19
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_deleteRelationshipIndex__19() {
          return __this.getServices(__cb(_, __frame, 2, 24, function ___(__0, __1) {
            services = __1;
            return __this._request.del({
              url: ((("" + services.relationship_index) + "/") + (encodeURIComponent(name)))
            }, __cb(_, __frame, 3, 33, function ___(__0, __2) {
              response = __2;
              if ((response.statusCode !== status.NO_CONTENT)) {
                return _(response);
              }
              ;
              __then();
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_deleteRelationshipIndex__19() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_deleteRelationshipIndex__19() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.execute"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>execute (script, params, callback)](#apidoc.element.neo4j.GraphDatabase.prototype.execute)
- description and source-code
```javascript
execute = function (script, params, callback) {
  if ((typeof params === "function")) {
    callback = params;
    params = null;
  }
  ;
  return actual.call(this, script, params, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.fromJSON"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>fromJSON (obj)](#apidoc.element.neo4j.GraphDatabase.prototype.fromJSON)
- description and source-code
```javascript
fromJSON = function (obj) {
  var Constructor, meta;
  meta = ((obj != null) ? obj[JSON_KEY] : void 0);
  if ((typeof (((meta != null) ? meta.constructor : void 0)) !== "string")) {
    throw new Error(("Invalid JSON object: " + (JSON.stringify(obj))));
  }
  ;
  Constructor = require(("./" + meta.constructor));
  return Constructor._fromJSON(this, obj);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.getIndexedNode"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getIndexedNode (index, property, value, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getIndexedNode)
- description and source-code
```javascript
function GraphDatabase_prototype_getIndexedNode__5(index, property, value, _) {
  var error, node, nodes, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_getIndexedNode__5",
    line: 206
  };
  return __func(_, this, arguments, GraphDatabase_prototype_getIndexedNode__5, 3, __frame, function __$GraphDatabase_prototype_getIndexedNode__5
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_getIndexedNode__5() {
          return __this.getIndexedNodes(index, property, value, __cb(_, __frame, 2, 21, function ___(__0, __1) {
            nodes = __1;
            node = null;
            if ((nodes && (nodes.length > 0))) {
              node = nodes[0];
            }
            ;
            return _(null, node);
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_getIndexedNode__5() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_getIndexedNode__5() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.getIndexedNodes"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getIndexedNodes (index, property, value, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getIndexedNodes)
- description and source-code
```javascript
function GraphDatabase_prototype_getIndexedNodes__6(index, property, value, _) {
  var error, key, response, services, url, val, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_getIndexedNodes__6",
    line: 232
  };
  return __func(_, this, arguments, GraphDatabase_prototype_getIndexedNodes__6, 3, __frame, function __$GraphDatabase_prototype_getIndexedNodes__6
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_getIndexedNodes__6() {
          return __this.getServices(__cb(_, __frame, 2, 24, function ___(__0, __1) {
            services = __1;
            key = encodeURIComponent(property);
            val = encodeURIComponent(value);
            url = ((((((("" + services.node_index) + "/") + index) + "/") + key) + "/") + val);
            return __this._request.get(url, __cb(_, __frame, 8, 33, function ___(__0, __2) {
              response = __2;
              if ((response.statusCode !== status.OK)) {
                return _(response);
              }
              ;
              return _(null, response.body.map((function(_this) {
                return function(node) {
                  return new Node(_this, node);
                };
              })(__this)));
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_getIndexedNodes__6() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_getIndexedNodes__6() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.getIndexedRelationship"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getIndexedRelationship (index, property, value, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getIndexedRelationship)
- description and source-code
```javascript
function GraphDatabase_prototype_getIndexedRelationship__11(index, property, value, _) {
  var error, relationships, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_getIndexedRelationship__11",
    line: 350
  };
  return __func(_, this, arguments, GraphDatabase_prototype_getIndexedRelationship__11, 3, __frame, function __$GraphDatabase_prototype_getIndexedRelationship__11
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_getIndexedRelationship__11() {
          return __this.getIndexedRelationships(index, property, value, __cb(_, __frame, 2, 29, function ___(__0, __1) {
            relationships = __1;
            return _(null, ((((relationships != null) ? relationships[0] : void 0)) || null));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_getIndexedRelationship__11() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_getIndexedRelationship__11() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.getIndexedRelationships"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getIndexedRelationships (index, property, value, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getIndexedRelationships)
- description and source-code
```javascript
function GraphDatabase_prototype_getIndexedRelationships__12(index, property, value, _) {
  var error, key, response, services, url, val, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_getIndexedRelationships__12",
    line: 373
  };
  return __func(_, this, arguments, GraphDatabase_prototype_getIndexedRelationships__12, 3, __frame, function __$GraphDatabase_prototype_getIndexedRelationships__12
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_getIndexedRelationships__12() {
          return __this.getServices(__cb(_, __frame, 2, 24, function ___(__0, __1) {
            services = __1;
            key = encodeURIComponent(property);
            val = encodeURIComponent(value);
            url = ((((((("" + services.relationship_index) + "/") + index) + "/") + key) + "/") + val);
            return __this._request.get(url, __cb(_, __frame, 8, 33, function ___(__0, __2) {
              response = __2;
              if ((response.statusCode !== status.OK)) {
                return _(response);
              }
              ;
              return _(null, response.body.map((function(_this) {
                return function(relationship) {
                  return new Relationship(_this, relationship);
                };
              })(__this)));
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_getIndexedRelationships__12() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_getIndexedRelationships__12() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.getNode"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getNode (url, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getNode)
- description and source-code
```javascript
function GraphDatabase_prototype_getNode__3(url, _) {
  var error, response, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_getNode__3",
    line: 149
  };
  return __func(_, this, arguments, GraphDatabase_prototype_getNode__3, 1, __frame, function __$GraphDatabase_prototype_getNode__3
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_getNode__3() {
          return __this._request.get(url, __cb(_, __frame, 2, 33, function ___(__0, __1) {
            response = __1;
            if ((response.statusCode !== status.OK)) {
              if ((response.statusCode === status.NOT_FOUND)) {
                return _(new Error(("No node at " + url)));
              }
              ;
              return _(response);
            }
            ;
            return _(null, new Node(__this, response.body));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_getNode__3() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_getNode__3() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.getNodeById"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getNodeById (id, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getNodeById)
- description and source-code
```javascript
function GraphDatabase_prototype_getNodeById__4(id, _) {
  var error, node, services, url, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_getNodeById__4",
    line: 178
  };
  return __func(_, this, arguments, GraphDatabase_prototype_getNodeById__4, 1, __frame, function __$GraphDatabase_prototype_getNodeById__4
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_getNodeById__4() {
          return __this.getServices(__cb(_, __frame, 2, 24, function ___(__0, __1) {
            services = __1;
            url = ((("" + services.node) + "/") + id);
            return __this.getNode(url, __cb(_, __frame, 4, 20, function ___(__0, __2) {
              node = __2;
              return _(null, node);
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_getNodeById__4() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_getNodeById__4() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.getNodeIndexes"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getNodeIndexes (_)](#apidoc.element.neo4j.GraphDatabase.prototype.getNodeIndexes)
- description and source-code
```javascript
function GraphDatabase_prototype_getNodeIndexes__14(_) {
  var arr, error, map, name, props, response, services, _ref, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_getNodeIndexes__14",
    line: 440
  };
  return __func(_, this, arguments, GraphDatabase_prototype_getNodeIndexes__14, 0, __frame, function __$GraphDatabase_prototype_getNodeIndexes__14
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_getNodeIndexes__14() {
          return __this.getServices(__cb(_, __frame, 2, 24, function ___(__0, __1) {
            services = __1;
            return __this._request.get(services.node_index, __cb(_, __frame, 3, 33, function ___(__0, __2) {
              response = __2;
              if ((((_ref = response.statusCode) !== status.OK) && (_ref !== status.NO_CONTENT))) {
                return _(response);
              }
              ;
              map = (response.body || {
              });
              arr = [];
              for (name in map) {
                props = map[name];
                arr.push(name);
                arr[name] = props;
              };
              return _(null, arr);
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_getNodeIndexes__14() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_getNodeIndexes__14() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.getRelationship"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getRelationship (url, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getRelationship)
- description and source-code
```javascript
function GraphDatabase_prototype_getRelationship__9(url, _) {
  var error, response, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_getRelationship__9",
    line: 300
  };
  return __func(_, this, arguments, GraphDatabase_prototype_getRelationship__9, 1, __frame, function __$GraphDatabase_prototype_getRelationship__9
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_getRelationship__9() {
          return __this._request.get(url, __cb(_, __frame, 2, 33, function ___(__0, __1) {
            response = __1;
            if ((response.statusCode !== status.OK)) {
              return _(response);
            }
            ;
            return _(null, new Relationship(__this, response.body));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_getRelationship__9() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_getRelationship__9() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.getRelationshipById"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getRelationshipById (id, _)](#apidoc.element.neo4j.GraphDatabase.prototype.getRelationshipById)
- description and source-code
```javascript
function GraphDatabase_prototype_getRelationshipById__10(id, _) {
  var relationshipURL, services, url, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_getRelationshipById__10",
    line: 325
  };
  return __func(_, this, arguments, GraphDatabase_prototype_getRelationshipById__10, 1, __frame, function __$GraphDatabase_prototype_getRelationshipById__10
() {
    return __this.getServices(__cb(_, __frame, 1, 20, function ___(__0, __1) {
      services = __1;
      relationshipURL = services.node.replace("node", "relationship");
      url = ((("" + relationshipURL) + "/") + id);
      return __this.getRelationship(url, __cb(_, __frame, 5, 9, _, true));
    }, true));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.getRelationshipIndexes"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getRelationshipIndexes (_)](#apidoc.element.neo4j.GraphDatabase.prototype.getRelationshipIndexes)
- description and source-code
```javascript
function GraphDatabase_prototype_getRelationshipIndexes__17(_) {
  var arr, error, map, name, props, response, services, _ref, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_getRelationshipIndexes__17",
    line: 533
  };
  return __func(_, this, arguments, GraphDatabase_prototype_getRelationshipIndexes__17, 0, __frame, function __$GraphDatabase_prototype_getRelationshipIndexes__17
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_getRelationshipIndexes__17() {
          return __this.getServices(__cb(_, __frame, 2, 24, function ___(__0, __1) {
            services = __1;
            return __this._request.get(services.relationship_index, __cb(_, __frame, 3, 33, function ___(__0, __2) {
              response = __2;
              if ((((_ref = response.statusCode) !== status.OK) && (_ref !== status.NO_CONTENT))) {
                return _(response);
              }
              ;
              map = (response.body || {
              });
              arr = [];
              for (name in map) {
                props = map[name];
                arr.push(name);
                arr[name] = props;
              };
              return _(null, arr);
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_getRelationshipIndexes__17() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_getRelationshipIndexes__17() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.getServices"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>getServices (_)](#apidoc.element.neo4j.GraphDatabase.prototype.getServices)
- description and source-code
```javascript
function GraphDatabase_prototype_getServices__2(_) {
  var error, response, root, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_getServices__2",
    line: 99
  };
  return __func(_, this, arguments, GraphDatabase_prototype_getServices__2, 0, __frame, function __$GraphDatabase_prototype_getServices__2
() {
    if ((__this._services != null)) {
      return _(null, __this._services);
    }
    ;
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_getServices__2() {
          return __this._getRoot(__cb(_, __frame, 5, 20, function ___(__0, __1) {
            root = __1;
            return __this._request.get(root.data, __cb(_, __frame, 6, 33, function ___(__0, __2) {
              response = __2;
              if ((response.statusCode !== status.OK)) {
                return _(response);
              }
              ;
              return _(null, __this._services = response.body);
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_getServices__2() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_getServices__2() {
        _();
      });
    });
  });
}
```
- example usage
```shell
...
      };
    }
    ;
    __then();
  }, true));
}
 else {
  return __this.db.getServices(__cb(_, __frame, 19, 31, function ___(__0, __2) {
    services = __2;
    return __this._request.post({
      uri: services.node,
      json: __this.data
    }, __cb(_, __frame, 21, 37, function ___(__0, __3) {
      response = __3;
      if ((response.statusCode !== status.CREATED)) {
...
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.query"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>query (query, params, callback)](#apidoc.element.neo4j.GraphDatabase.prototype.query)
- description and source-code
```javascript
query = function (query, params, callback) {
  if (((typeof query === "function") && (typeof params === "string"))) {
    console.warn((("neo4j.GraphDatabase::query()’s signature is " + "now (query, params, callback). Please update your code!\n") +
new Error().stack.split("\n")[2]));
    callback = query;
    query = params;
    params = null;
  }
   else if ((typeof params === "function")) {
    callback = params;
    params = null;
  }

  ;
  return actual.call(this, query, params, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.queryNodeIndex"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>queryNodeIndex (index, query, _)](#apidoc.element.neo4j.GraphDatabase.prototype.queryNodeIndex)
- description and source-code
```javascript
function GraphDatabase_prototype_queryNodeIndex__7(index, query, _) {
  var error, response, services, url, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_queryNodeIndex__7",
    line: 264
  };
  return __func(_, this, arguments, GraphDatabase_prototype_queryNodeIndex__7, 2, __frame, function __$GraphDatabase_prototype_queryNodeIndex__7
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_queryNodeIndex__7() {
          return __this.getServices(__cb(_, __frame, 2, 24, function ___(__0, __1) {
            services = __1;
            url = ((((("" + services.node_index) + "/") + index) + "?query=") + (encodeURIComponent(query)));
            return __this._request.get(url, __cb(_, __frame, 5, 33, function ___(__0, __2) {
              response = __2;
              if ((response.statusCode !== status.OK)) {
                return _(response);
              }
              ;
              return _(null, response.body.map((function(_this) {
                return function(node) {
                  return new Node(_this, node);
                };
              })(__this)));
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_queryNodeIndex__7() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_queryNodeIndex__7() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.queryRelationshipIndex"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>queryRelationshipIndex (index, query, _)](#apidoc.element.neo4j.GraphDatabase.prototype.queryRelationshipIndex)
- description and source-code
```javascript
function GraphDatabase_prototype_queryRelationshipIndex__13(index, query, _) {
  var error, response, services, url, __this = this;
  var __frame = {
    name: "GraphDatabase_prototype_queryRelationshipIndex__13",
    line: 405
  };
  return __func(_, this, arguments, GraphDatabase_prototype_queryRelationshipIndex__13, 2, __frame, function __$GraphDatabase_prototype_queryRelationshipIndex__13
() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$GraphDatabase_prototype_queryRelationshipIndex__13() {
          return __this.getServices(__cb(_, __frame, 2, 24, function ___(__0, __1) {
            services = __1;
            url = ((((("" + services.relationship_index) + "/") + index) + "?query=") + (encodeURIComponent(query)));
            return __this._request.get(url, __cb(_, __frame, 5, 33, function ___(__0, __2) {
              response = __2;
              if ((response.statusCode !== status.OK)) {
                return _(response);
              }
              ;
              return _(null, response.body.map((function(_this) {
                return function(relationship) {
                  return new Relationship(_this, relationship);
                };
              })(__this)));
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$GraphDatabase_prototype_queryRelationshipIndex__13() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$GraphDatabase_prototype_queryRelationshipIndex__13() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.GraphDatabase.prototype.reviveJSON"></a>[function <span class="apidocSignatureSpan">neo4j.GraphDatabase.prototype.</span>reviveJSON (key, val)](#apidoc.element.neo4j.GraphDatabase.prototype.reviveJSON)
- description and source-code
```javascript
reviveJSON = function (key, val) {
  var _ref;
  if ((typeof (((val != null) ? (((_ref = val[JSON_KEY]) != null) ? _ref.constructor : void 0) : void 0)) === "string")) {
    return this.fromJSON(val);
  }
   else {
    return val;
  }
  ;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.neo4j.Node"></a>[module neo4j.Node](#apidoc.module.neo4j.Node)

#### <a name="apidoc.element.neo4j.Node.Node"></a>[function <span class="apidocSignatureSpan">neo4j.</span>Node (db, data)](#apidoc.element.neo4j.Node.Node)
- description and source-code
```javascript
function Node(db, data) {
  Node.__super__.constructor.call(this, db, data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node._fromJSON"></a>[function <span class="apidocSignatureSpan">neo4j.Node.</span>_fromJSON (db, obj)](#apidoc.element.neo4j.Node._fromJSON)
- description and source-code
```javascript
_fromJSON = function (db, obj) {
  var _data;
  _data = obj._data;
  return new this(db, _data);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.neo4j.Node.prototype"></a>[module neo4j.Node.prototype](#apidoc.module.neo4j.Node.prototype)

#### <a name="apidoc.element.neo4j.Node.prototype._createRelationship"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>_createRelationship (from, to, type, data, _)](#apidoc.element.neo4j.Node.prototype._createRelationship)
- description and source-code
```javascript
function Node_prototype__createRelationship__5(from, to, type, data, _) {
  var createRelationshipURL, error, exception, message, otherNodeURL, response, _ref, __this = this;
  var __frame = {
    name: "Node_prototype__createRelationship__5",
    line: 250
  };
  return __func(_, this, arguments, Node_prototype__createRelationship__5, 4, __frame, function __$Node_prototype__createRelationship__5
() {
    if ((data == null)) {
      data = {
      };
    }
    ;
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$Node_prototype__createRelationship__5() {
          createRelationshipURL = from._data["create_relationship"];
          otherNodeURL = to.self;
          return (function __$Node_prototype__createRelationship__5(__then) {
            if ((((createRelationshipURL != null)) && otherNodeURL)) {
              return __this._request.post({
                url: createRelationshipURL,
                json: {
                  to: otherNodeURL,
                  data: data,
                  type: type
                }
              }, __cb(_, __frame, 11, 37, function ___(__0, __2) {
                response = __2;
                return (function __$Node_prototype__createRelationship__5(__then) {
                  if ((response.statusCode !== status.CREATED)) {
                    _ref = (response.body || {
                    }), message = _ref.message, exception = _ref.exception;
                    return (function __$Node_prototype__createRelationship__5(_) {
                      var __1 = message;
                      if (__1) {
                        return _(null, __1);
                      }
                      ;
                      return (function __$Node_prototype__createRelationship__5(_) {
                        var __2 = exception;
                        if (__2) {
                          return _(null, __2);
                        }
                        ;
                        return (function ___closure(_) {
                          switch (response.statusCode) {
                          case status.BAD_REQUEST:
                            return _(null, ((((((("Invalid createRelationship: " + from.id) + " ") + type) + " ") + to.id) + " w
/ data: ") + (JSON.stringify(data))));
                          case status.CONFLICT:
                            return _(null, "\"to\" node, or the node specified by the URI not found");
                            default:
                            return _(response);
                          };
                          _();
                        })(__cb(_, __frame, 22, 32, _, true));
                      })(__cb(_, __frame, -249, 0, function ___(__0, __4) {
                        var __3 = (message = __4);
                        return _(null, __3);
                      }, true));
                    })(__cb(_, __frame, -249, 0, function __$Node_prototype__createRelationship__5() {
                      return _(new Error(message));
                    }, true));
                  }
                   else {
                    __then();
                  }
                  ;
                })(function __$Node_prototype__createRelationship__5() {
                  return _(null, new Relationship(__this.db, response.body, from, to));
                });
              }, true));
            }
             else {
              return _(new Error("Failed to create relationship"));
            }
            ;
          })(__then);
        });
      })(function ___(_error, __result) {
        __catch(function __$Node_prototype__createRelationship__5() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$Node_prototype__createRelationship__5() {
        _();
      });
    });
  });
}
```
- example usage
```shell
...
})(Node.prototype.unindex);
Node.prototype.createRelationshipTo = function(otherNode, type, data, cb) {
  if ((typeof data === "function")) {
    cb = data;
    data = null;
  }
  ;
  return this._createRelationship(this, otherNode, type, data, cb);
};
Node.prototype.createRelationshipFrom = function(otherNode, type, data, cb) {
  if ((typeof data === "function")) {
    cb = data;
    data = null;
  }
  ;
...
```

#### <a name="apidoc.element.neo4j.Node.prototype._getRelationships"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>_getRelationships (direction, type, _)](#apidoc.element.neo4j.Node.prototype._getRelationships)
- description and source-code
```javascript
function Node_prototype__getRelationships__6(direction, type, _) {
  var error, prefix, relationshipsURL, resp, types, __this = this;
  var __frame = {
    name: "Node_prototype__getRelationships__6",
    line: 308
  };
  return __func(_, this, arguments, Node_prototype__getRelationships__6, 2, __frame, function __$Node_prototype__getRelationships__6
() {
    types = null;
    if ((type != null)) {
      types = ((type instanceof Array) ? type : [type,]);
    }
    ;
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$Node_prototype__getRelationships__6() {
          if ((types != null)) {
            prefix = __this._data[(("" + direction) + "_typed_relationships")];
            relationshipsURL = ((prefix != null) ? prefix.replace("{-list|&|types}", types.join("&")) : void 0);
          }
           else {
            relationshipsURL = __this._data[(("" + direction) + "_relationships")];
          }
          ;
          if (!relationshipsURL) {
            return _(new Error("Couldn't find URL of relationships endpoint."));
          }
          ;
          return __this._request.get(relationshipsURL, __cb(_, __frame, 25, 29, function ___(__0, __1) {
            resp = __1;
            if ((resp.statusCode === status.NOT_FOUND)) {
              return _(new Error("Node not found."));
            }
            ;
            if ((resp.statusCode !== status.OK)) {
              return _(new Error(("Unrecognized response code: " + resp.statusCode)));
            }
            ;
            return _(null, resp.body.map((function(_this) {
              return function(data) {
                if ((_this.self === data.start)) {
                  return new Relationship(_this.db, data, _this, null);
                }
                 else {
                  return new Relationship(_this.db, data, null, _this);
                }
                ;
              };
            })(__this)));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$Node_prototype__getRelationships__6() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$Node_prototype__getRelationships__6() {
        _();
      });
    });
  });
}
```
- example usage
```shell
...
Node.prototype.outgoing = function Node_prototype_outgoing__8(type, _) {
  var __this = this;
  var __frame = {
    name: "Node_prototype_outgoing__8",
    line: 371
  };
  return __func(_, this, arguments, Node_prototype_outgoing__8, 1, __frame, function __$Node_prototype_outgoing__8() {
    return __this._getRelationships("outgoing", type, __cb(_, __frame, 1, 9, _, true));
  });
};
Node.prototype.incoming = function Node_prototype_incoming__9(type, _) {
  var __this = this;
  var __frame = {
    name: "Node_prototype_incoming__9",
    line: 382
...
```

#### <a name="apidoc.element.neo4j.Node.prototype.all"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>all (type, _)](#apidoc.element.neo4j.Node.prototype.all)
- description and source-code
```javascript
function Node_prototype_all__10(type, _) {
  var __this = this;
  var __frame = {
    name: "Node_prototype_all__10",
    line: 395
  };
  return __func(_, this, arguments, Node_prototype_all__10, 1, __frame, function __$Node_prototype_all__10() {
    return __this._getRelationships("all", type, __cb(_, __frame, 1, 9, _, true));
  });
}
```
- example usage
```shell
...
}
;
return (function ___(__then) {
  (function ___(_) {
    __tryCatch(_, function __$Node_prototype_delete__2() {
      return (function __$Node_prototype_delete__2(__then) {
        if (force) {
          return __this.all(null, __cb(_, __frame, 8, 33, function ___(__0, __2) {
            relationships = __2;
            return relationships.forEach_(__cb(_, __frame, 9, 30, __then, true), {
              parallel: true
            }, function __1(_, rel) {
              var __frame = {
                name: "__1",
                line: 106
...
```

#### <a name="apidoc.element.neo4j.Node.prototype.constructor"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>constructor (db, data)](#apidoc.element.neo4j.Node.prototype.constructor)
- description and source-code
```javascript
function Node(db, data) {
  Node.__super__.constructor.call(this, db, data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node.prototype.createRelationshipFrom"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>createRelationshipFrom (otherNode, type, data, cb)](#apidoc.element.neo4j.Node.prototype.createRelationshipFrom)
- description and source-code
```javascript
createRelationshipFrom = function (otherNode, type, data, cb) {
  if ((typeof data === "function")) {
    cb = data;
    data = null;
  }
  ;
  return this._createRelationship(otherNode, this, type, data, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node.prototype.createRelationshipTo"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>createRelationshipTo (otherNode, type, data, cb)](#apidoc.element.neo4j.Node.prototype.createRelationshipTo)
- description and source-code
```javascript
createRelationshipTo = function (otherNode, type, data, cb) {
  if ((typeof data === "function")) {
    cb = data;
    data = null;
  }
  ;
  return this._createRelationship(this, otherNode, type, data, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node.prototype.delete"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>delete (_, force)](#apidoc.element.neo4j.Node.prototype.delete)
- description and source-code
```javascript
function Node_prototype_delete__2(_, force) {
  var error, relationships, __this = this, __arguments = arguments;
  var __frame = {
    name: "Node_prototype_delete__2",
    line: 97
  };
  return __func(_, this, arguments, Node_prototype_delete__2, 0, __frame, function __$Node_prototype_delete__2() {
    if ((force == null)) {
      force = false;
    }
    ;
    if (!__this.exists) {
      return _(null);
    }
    ;
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$Node_prototype_delete__2() {
          return (function __$Node_prototype_delete__2(__then) {
            if (force) {
              return __this.all(null, __cb(_, __frame, 8, 33, function ___(__0, __2) {
                relationships = __2;
                return relationships.forEach_(__cb(_, __frame, 9, 30, __then, true), {
                  parallel: true
                }, function __1(_, rel) {
                  var __frame = {
                    name: "__1",
                    line: 106
                  };
                  return __func(_, this, arguments, __1, 0, __frame, function __$__1() {
                    return rel["delete"](__cb(_, __frame, 1, 20, _, true));
                  });
                });
              }, true));
            }
             else {
              __then();
            }
            ;
          })(__then);
        });
      })(function ___(_error, __result) {
        __catch(function __$Node_prototype_delete__2() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$Node_prototype_delete__2() {
        return __apply(__cb(_, __frame, NaN, 0, _, true), Node.__super__["delete"], __this, __arguments, 0);
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node.prototype.getRelationshipNodes"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>getRelationshipNodes (rels, _)](#apidoc.element.neo4j.Node.prototype.getRelationshipNodes)
- description and source-code
```javascript
function Node_prototype_getRelationshipNodes__11(rels, _) {
  var error, resp, traverseURL, _ref, _ref1, _ref2, __this = this;
  var __frame = {
    name: "Node_prototype_getRelationshipNodes__11",
    line: 414
  };
  return __func(_, this, arguments, Node_prototype_getRelationshipNodes__11, 1, __frame, function __$Node_prototype_getRelationshipNodes__11
() {
    rels = ((rels instanceof Array) ? rels : [rels,]);
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$Node_prototype_getRelationshipNodes__11() {
          traverseURL = (((_ref = __this._data["traverse"]) != null) ? _ref.replace("{returnType}", "node") : void 0);
          if (!traverseURL) {
            return _(new Error("Traverse not available."));
          }
          ;
          return __this._request.post({
            url: traverseURL,
            json: {
              max_depth: 1,
              relationships: rels.map(function(rel) {
                if ((typeof rel === "string")) {
                  return {
                    type: rel
                  };
                }
                 else {
                  return rel;
                }
                ;
              })
            }
          }, __cb(_, __frame, 11, 29, function ___(__0, __1) {
            resp = __1;
            if ((resp.statusCode === 404)) {
              return _(new Error((((((_ref1 = resp.body) != null) ? _ref1.message : void 0)) || "Node not found.")));
            }
            ;
            if ((resp.statusCode !== 200)) {
              return _(new Error((((((_ref2 = resp.body) != null) ? _ref2.message : void 0)) || (("Unrecognized response code: " +
resp.statusCode)))));
            }
            ;
            return _(null, resp.body.map((function(_this) {
              return function(data) {
                return new Node(_this.db, data);
              };
            })(__this)));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$Node_prototype_getRelationshipNodes__11() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$Node_prototype_getRelationshipNodes__11() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node.prototype.getRelationships"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>getRelationships (type, _)](#apidoc.element.neo4j.Node.prototype.getRelationships)
- description and source-code
```javascript
function Node_prototype_getRelationships__7(type, _) {
  var __this = this;
  var __frame = {
    name: "Node_prototype_getRelationships__7",
    line: 360
  };
  return __func(_, this, arguments, Node_prototype_getRelationships__7, 1, __frame, function __$Node_prototype_getRelationships__7
() {
    return __this.all(type, __cb(_, __frame, 1, 9, _, true));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node.prototype.incoming"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>incoming (type, _)](#apidoc.element.neo4j.Node.prototype.incoming)
- description and source-code
```javascript
function Node_prototype_incoming__9(type, _) {
  var __this = this;
  var __frame = {
    name: "Node_prototype_incoming__9",
    line: 382
  };
  return __func(_, this, arguments, Node_prototype_incoming__9, 1, __frame, function __$Node_prototype_incoming__9() {
    return __this._getRelationships("incoming", type, __cb(_, __frame, 1, 9, _, true));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node.prototype.index"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>index (index, key, value, _)](#apidoc.element.neo4j.Node.prototype.index)
- description and source-code
```javascript
function Node_prototype_index__3(index, key, value, _) {
  var error, response, services, __this = this;
  var __frame = {
    name: "Node_prototype_index__3",
    line: 123
  };
  return __func(_, this, arguments, Node_prototype_index__3, 3, __frame, function __$Node_prototype_index__3() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$Node_prototype_index__3() {
          if (!__this.exists) {
            return _(new Error("Node must exist before indexing."));
          }
          ;
          return __this.db.getServices(__cb(_, __frame, 5, 27, function ___(__0, __1) {
            services = __1;
            return __this._request.post({
              url: ((("" + services.node_index) + "/") + index),
              json: {
                key: key,
                value: value,
                uri: __this.self
              }
            }, __cb(_, __frame, 7, 33, function ___(__0, __2) {
              response = __2;
              if ((response.statusCode !== status.CREATED)) {
                return _(response);
              }
              ;
              __then();
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$Node_prototype_index__3() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$Node_prototype_index__3() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node.prototype.outgoing"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>outgoing (type, _)](#apidoc.element.neo4j.Node.prototype.outgoing)
- description and source-code
```javascript
function Node_prototype_outgoing__8(type, _) {
  var __this = this;
  var __frame = {
    name: "Node_prototype_outgoing__8",
    line: 371
  };
  return __func(_, this, arguments, Node_prototype_outgoing__8, 1, __frame, function __$Node_prototype_outgoing__8() {
    return __this._getRelationships("outgoing", type, __cb(_, __frame, 1, 9, _, true));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node.prototype.path"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>path (to, type, direction, maxDepth, algorithm, _)](#apidoc.element.neo4j.Node.prototype.path)
- description and source-code
```javascript
function Node_prototype_path__12(to, type, direction, maxDepth, algorithm, _) {
  var data, end, error, length, nodes, pathURL, relationships, res, start, __this = this;
  var __frame = {
    name: "Node_prototype_path__12",
    line: 463
  };
  return __func(_, this, arguments, Node_prototype_path__12, 5, __frame, function __$Node_prototype_path__12() {
    if ((maxDepth == null)) {
      maxDepth = 1;
    }
    ;
    if ((algorithm == null)) {
      algorithm = "shortestPath";
    }
    ;
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$Node_prototype_path__12() {
          pathURL = (("" + __this.self) + "/path");
          data = {
            to: to.self,
            relationships: {
              type: type,
              direction: direction
            },
            max_depth: maxDepth,
            algorithm: algorithm
          };
          return __this._request.post({
            url: pathURL,
            json: data
          }, __cb(_, __frame, 11, 28, function ___(__0, __1) {
            res = __1;
            if ((res.statusCode === status.NOT_FOUND)) {
              return _(null, null);
            }
            ;
            if ((res.statusCode !== status.OK)) {
              return _(new Error(("Unrecognized response code: " + res.statusCode)));
            }
            ;
            data = res.body;
            start = new Node(__this, {
              self: data.start
            });
            end = new Node(__this, {
              self: data.end
            });
            length = data.length;
            nodes = data.nodes.map((function(_this) {
              return function(url) {
                return new Node(_this, {
                  self: url
                });
              };
            })(__this));
            relationships = data.relationships.map((function(_this) {
              return function(url) {
                return new Relationship(_this, {
                  self: url,
                  type: type
                });
              };
            })(__this));
            return _(null, new Path(start, end, length, nodes, relationships));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$Node_prototype_path__12() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$Node_prototype_path__12() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node.prototype.save"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>save (_)](#apidoc.element.neo4j.Node.prototype.save)
- description and source-code
```javascript
function Node_prototype_save__1(_) {
  var error, response, services, __this = this;
  var __frame = {
    name: "Node_prototype_save__1",
    line: 43
  };
  return __func(_, this, arguments, Node_prototype_save__1, 0, __frame, function __$Node_prototype_save__1() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$Node_prototype_save__1() {
          return (function __$Node_prototype_save__1(__then) {
            if (__this.exists) {
              return __this._request.put({
                uri: (("" + __this.self) + "/properties"),
                json: __this.data
              }, __cb(_, __frame, 4, 37, function ___(__0, __1) {
                response = __1;
                if ((response.statusCode !== status.NO_CONTENT)) {
                  switch (response.statusCode) {
                  case status.BAD_REQUEST:
                    return _(new Error("Invalid data sent"));
                  case status.NOT_FOUND:
                    return _(new Error("Node not found"));
                    default:
                    return _(response);
                  };
                }
                ;
                __then();
              }, true));
            }
             else {
              return __this.db.getServices(__cb(_, __frame, 19, 31, function ___(__0, __2) {
                services = __2;
                return __this._request.post({
                  uri: services.node,
                  json: __this.data
                }, __cb(_, __frame, 21, 37, function ___(__0, __3) {
                  response = __3;
                  if ((response.statusCode !== status.CREATED)) {
                    switch (response.statusCode) {
                    case status.BAD_REQUEST:
                      return _(new Error("Invalid data sent"));
                      default:
                      return _(response);
                    };
                  }
                  ;
                  __this._data = response.body;
                  __then();
                }, true));
              }, true));
            }
            ;
          })(function __$Node_prototype_save__1() {
            return _(null, __this);
          });
        });
      })(function ___(_error, __result) {
        __catch(function __$Node_prototype_save__1() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$Node_prototype_save__1() {
        _();
      });
    });
  });
}
```
- example usage
```shell
...
callbacks and return immediately, with the callbacks being invoked when the
corresponding HTTP requests and responses finish.

Here's a simple example:

'''js
var node = db.createNode({hello: 'world'});     // instantaneous, but...
node.save(function (err, node) {    // ...this is what actually persists.
    if (err) {
        console.error('Error saving new node to database:', err);
    } else {
        console.log('Node saved to database with id:', node.id);
    }
});
'''
...
```

#### <a name="apidoc.element.neo4j.Node.prototype.toString"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>toString ()](#apidoc.element.neo4j.Node.prototype.toString)
- description and source-code
```javascript
toString = function () {
  if (this.exists) {
    return ("node @" + this.id);
  }
   else {
    return (("unsaved node (" + (JSON.stringify(this.data, null, 4))) + ")");
  }
  ;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Node.prototype.unindex"></a>[function <span class="apidocSignatureSpan">neo4j.Node.prototype.</span>unindex (index, key, value, callback)](#apidoc.element.neo4j.Node.prototype.unindex)
- description and source-code
```javascript
unindex = function (index, key, value, callback) {
  if ((typeof key === "function")) {
    callback = key;
    key = null;
    value = null;
  }
   else if ((typeof value === "function")) {
    callback = value;
    value = null;
  }

  ;
  return actual.call(this, index, key, value, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.neo4j.PropertyContainer"></a>[module neo4j.PropertyContainer](#apidoc.module.neo4j.PropertyContainer)

#### <a name="apidoc.element.neo4j.PropertyContainer.PropertyContainer"></a>[function <span class="apidocSignatureSpan">neo4j.</span>PropertyContainer (db, data)](#apidoc.element.neo4j.PropertyContainer.PropertyContainer)
- description and source-code
```javascript
function PropertyContainer(db, data) {
  this.db = db;
  this._request = db._request;
  this._data = (data || {
  });
  this._data.self = ((((data != null) ? data.self : void 0)) || null);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.PropertyContainer._fromJSON"></a>[function <span class="apidocSignatureSpan">neo4j.PropertyContainer.</span>_fromJSON (db, obj)](#apidoc.element.neo4j.PropertyContainer._fromJSON)
- description and source-code
```javascript
_fromJSON = function (db, obj) {
  var _data;
  _data = obj._data;
  return new this(db, _data);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.neo4j.PropertyContainer.prototype"></a>[module neo4j.PropertyContainer.prototype](#apidoc.module.neo4j.PropertyContainer.prototype)

#### <a name="apidoc.element.neo4j.PropertyContainer.prototype.del"></a>[function <span class="apidocSignatureSpan">neo4j.PropertyContainer.prototype.</span>del ()](#apidoc.element.neo4j.PropertyContainer.prototype.del)
- description and source-code
```javascript
del = function () {
  return this["delete"].apply(this, arguments);
}
```
- example usage
```shell
...
;
if (value) {
  value = encodeURIComponent(value);
}
;
base = ((("" + services.node_index) + "/") + (encodeURIComponent(index)));
url = ((key && value) ? ((((((("" + base) + "/") + key) + "/") + value) + "/") + __this.id) : (key ? ((((("" + base) + "/") + key
) + "/") + __this.id) : ((("" + base) + "/") + __this.id)));
return __this._request.del(url, __cb(_, __frame, 20, 33, function ___(__0, __2) {
  response = __2;
  if ((response.statusCode !== status.NO_CONTENT)) {
    return _(response);
  }
  ;
  __then();
}, true));
...
```

#### <a name="apidoc.element.neo4j.PropertyContainer.prototype.delete"></a>[function <span class="apidocSignatureSpan">neo4j.PropertyContainer.prototype.</span>delete (_)](#apidoc.element.neo4j.PropertyContainer.prototype.delete)
- description and source-code
```javascript
function PropertyContainer_prototype_delete__1(_) {
  var error, response, __this = this;
  var __frame = {
    name: "PropertyContainer_prototype_delete__1",
    line: 86
  };
  return __func(_, this, arguments, PropertyContainer_prototype_delete__1, 0, __frame, function __$PropertyContainer_prototype_delete__1
() {
    if (!__this.exists) {
      return _(null);
    }
    ;
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$PropertyContainer_prototype_delete__1() {
          return __this._request.del(__this.self, __cb(_, __frame, 5, 33, function ___(__0, __1) {
            response = __1;
            if ((response.statusCode !== status.NO_CONTENT)) {
              switch (response.statusCode) {
              case status.NOT_FOUND:
                return _(new Error("PropertyContainer not found"));
              case status.CONFLICT:
                return _(new Error("Node could not be deleted (still has relationships?)"));
                default:
                return _(response);
              };
            }
            ;
            __this._data.self = null;
            __then();
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$PropertyContainer_prototype_delete__1() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$PropertyContainer_prototype_delete__1() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.PropertyContainer.prototype.equals"></a>[function <span class="apidocSignatureSpan">neo4j.PropertyContainer.prototype.</span>equals (other)](#apidoc.element.neo4j.PropertyContainer.prototype.equals)
- description and source-code
```javascript
equals = function (other) {
  return (this.self === (((other != null) ? other.self : void 0)));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.PropertyContainer.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">neo4j.PropertyContainer.prototype.</span>toJSON ()](#apidoc.element.neo4j.PropertyContainer.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  var json;
  json = this.db._toJSON(this);
  json._data = this._data;
  return json;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.neo4j.Relationship"></a>[module neo4j.Relationship](#apidoc.module.neo4j.Relationship)

#### <a name="apidoc.element.neo4j.Relationship.Relationship"></a>[function <span class="apidocSignatureSpan">neo4j.</span>Relationship (db, data, start, end)](#apidoc.element.neo4j.Relationship.Relationship)
- description and source-code
```javascript
function Relationship(db, data, start, end) {
  var Node;
  Relationship.__super__.constructor.call(this, db, data);
  Node = require("./Node");
  this._start = (start || new Node(db, {
    self: data.start
  }));
  this._end = (end || new Node(db, {
    self: data.end
  }));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Relationship._fromJSON"></a>[function <span class="apidocSignatureSpan">neo4j.Relationship.</span>_fromJSON (db, obj)](#apidoc.element.neo4j.Relationship._fromJSON)
- description and source-code
```javascript
_fromJSON = function (db, obj) {
  var _data;
  _data = obj._data;
  return new this(db, _data);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.neo4j.Relationship.prototype"></a>[module neo4j.Relationship.prototype](#apidoc.module.neo4j.Relationship.prototype)

#### <a name="apidoc.element.neo4j.Relationship.prototype.constructor"></a>[function <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>constructor (db, data, start, end)](#apidoc.element.neo4j.Relationship.prototype.constructor)
- description and source-code
```javascript
function Relationship(db, data, start, end) {
  var Node;
  Relationship.__super__.constructor.call(this, db, data);
  Node = require("./Node");
  this._start = (start || new Node(db, {
    self: data.start
  }));
  this._end = (end || new Node(db, {
    self: data.end
  }));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Relationship.prototype.index"></a>[function <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>index (index, key, value, _)](#apidoc.element.neo4j.Relationship.prototype.index)
- description and source-code
```javascript
function Relationship_prototype_index__2(index, key, value, _) {
  var error, response, services, __this = this;
  var __frame = {
    name: "Relationship_prototype_index__2",
    line: 111
  };
  return __func(_, this, arguments, Relationship_prototype_index__2, 3, __frame, function __$Relationship_prototype_index__2() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$Relationship_prototype_index__2() {
          if (!__this.exists) {
            return _(new Error("Relationship must exist before indexing properties"));
          }
          ;
          return __this.db.getServices(__cb(_, __frame, 5, 27, function ___(__0, __1) {
            services = __1;
            return __this._request.post({
              url: ((("" + services.relationship_index) + "/") + index),
              json: {
                key: key,
                value: value,
                uri: __this.self
              }
            }, __cb(_, __frame, 7, 33, function ___(__0, __2) {
              response = __2;
              if ((response.statusCode !== status.CREATED)) {
                return _(response);
              }
              ;
              __then();
            }, true));
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$Relationship_prototype_index__2() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$Relationship_prototype_index__2() {
        _();
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Relationship.prototype.save"></a>[function <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>save (_)](#apidoc.element.neo4j.Relationship.prototype.save)
- description and source-code
```javascript
function Relationship_prototype_save__1(_) {
  var error, response, __this = this;
  var __frame = {
    name: "Relationship_prototype_save__1",
    line: 78
  };
  return __func(_, this, arguments, Relationship_prototype_save__1, 0, __frame, function __$Relationship_prototype_save__1() {
    return (function ___(__then) {
      (function ___(_) {
        __tryCatch(_, function __$Relationship_prototype_save__1() {
          return __this._request.put({
            uri: (("" + __this.self) + "/properties"),
            json: __this.data
          }, __cb(_, __frame, 4, 33, function ___(__0, __1) {
            response = __1;
            if ((response.statusCode !== status.NO_CONTENT)) {
              switch (response.statusCode) {
              case status.BAD_REQUEST:
                return _(new Error("Invalid data sent"));
              case status.NOT_FOUND:
                return _(new Error("Relationship not found"));
                default:
                return _(response);
              };
            }
            ;
            return _(null, __this);
          }, true));
        });
      })(function ___(_error, __result) {
        __catch(function __$Relationship_prototype_save__1() {
          if (_error) {
            error = _error;
            return _(adjustError(error));
          }
           else {
            _(null, __result);
          }
          ;
        }, _);
      });
    })(function ___() {
      __tryCatch(_, function __$Relationship_prototype_save__1() {
        _();
      });
    });
  });
}
```
- example usage
```shell
...
callbacks and return immediately, with the callbacks being invoked when the
corresponding HTTP requests and responses finish.

Here's a simple example:

'''js
var node = db.createNode({hello: 'world'});     // instantaneous, but...
node.save(function (err, node) {    // ...this is what actually persists.
    if (err) {
        console.error('Error saving new node to database:', err);
    } else {
        console.log('Node saved to database with id:', node.id);
    }
});
'''
...
```

#### <a name="apidoc.element.neo4j.Relationship.prototype.toString"></a>[function <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>toString ()](#apidoc.element.neo4j.Relationship.prototype.toString)
- description and source-code
```javascript
toString = function () {
  return (((("relationship @" + this.id) + " (") + this.type) + ")");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.Relationship.prototype.unindex"></a>[function <span class="apidocSignatureSpan">neo4j.Relationship.prototype.</span>unindex (index, key, value, callback)](#apidoc.element.neo4j.Relationship.prototype.unindex)
- description and source-code
```javascript
unindex = function (index, key, value, callback) {
  if ((typeof key === "function")) {
    callback = key;
    key = null;
    value = null;
  }
   else if ((typeof value === "function")) {
    callback = value;
    value = null;
  }

  ;
  return actual.call(this, index, key, value, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.neo4j.util"></a>[module neo4j.util](#apidoc.module.neo4j.util)

#### <a name="apidoc.element.neo4j.util.adjustError"></a>[function <span class="apidocSignatureSpan">neo4j.util.</span>adjustError (error)](#apidoc.element.neo4j.util.adjustError)
- description and source-code
```javascript
adjustError = function (error) {
  var serverError;
  if (error.statusCode) {
    serverError = error.body || {
      message: "Unknown Neo4j error (status " + error.statusCode + ")."
    };
    if (typeof serverError === 'string') {
      try {
        serverError = JSON.parse(serverError);
      } catch (_error) {}
    }
    if ((serverError != null ? serverError.exception : void 0) && !serverError.message) {
      serverError.message = "Neo4j " + serverError.exception + ": " + (JSON.stringify(serverError.stacktrace || [], null, 2));
    }
    error = new Error;
    error.message = serverError.message || serverError;
  }
  if (typeof error !== 'object') {
    error = new Error(error);
  }
  if (error.code === 'ECONNREFUSED') {
    error.message = "Couldn't reach database (connection refused).";
  }
  return error;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.util.deserialize"></a>[function <span class="apidocSignatureSpan">neo4j.util.</span>deserialize (o, separator)](#apidoc.element.neo4j.util.deserialize)
- description and source-code
```javascript
deserialize = function (o, separator) {
  return unflatten(JSON.parse(o), separator);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.util.serialize"></a>[function <span class="apidocSignatureSpan">neo4j.util.</span>serialize (o, separator)](#apidoc.element.neo4j.util.serialize)
- description and source-code
```javascript
serialize = function (o, separator) {
  return JSON.stringify(flatten(o, separator));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.util.transform"></a>[function <span class="apidocSignatureSpan">neo4j.util.</span>transform (val, db)](#apidoc.element.neo4j.util.transform)
- description and source-code
```javascript
transform = function (val, db) {
  var Node, Path, Relationship, end, hasProps, key, length, map, nodes, relationships, start, subval;
  if (!val || typeof val !== 'object') {
    return val;
  }
  if (val instanceof Array) {
    return val.map(function(val) {
      return transform(val, db);
    });
  }
  Path = require('./Path');
  Node = require('./Node');
  Relationship = require('./Relationship');
  hasProps = function(props) {
    var key, keys, type, _i, _len, _ref;
    for (type in props) {
      keys = props[type];
      _ref = keys.split('|');
      for (_i = 0, _len = _ref.length; _i < _len; _i++) {
        key = _ref[_i];
        if (typeof val[key] !== type) {
          return false;
        }
      }
    }
    return true;
  };
  if (hasProps({
    string: 'self|traverse',
    object: 'data'
  })) {
    return new Node(db, val);
  }
  if (hasProps({
    string: 'self|type|start|end',
    object: 'data'
  })) {
    return new Relationship(db, val);
  }
  if (hasProps({
    string: 'start|end',
    number: 'length',
    object: 'nodes|relationships'
  })) {
    start = new Node(db, {
      self: val.start
    });
    end = new Node(db, {
      self: val.end
    });
    length = val.length;
    nodes = val.nodes.map(function(url) {
      return new Node(db, {
        self: url
      });
    });
    relationships = val.relationships.map(function(url) {
      return new Relationship(db, {
        self: url
      });
    });
    return new Path(start, end, length, nodes, relationships);
  } else {
    map = {};
    for (key in val) {
      subval = val[key];
      map[key] = transform(subval, db);
    }
    return map;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.neo4j.util.wrapRequest"></a>[function <span class="apidocSignatureSpan">neo4j.util.</span>wrapRequest (_arg)](#apidoc.element.neo4j.util.wrapRequest)
- description and source-code
```javascript
wrapRequest = function (_arg) {
  var auth, modifyArgs, proxy, req, url, verb, wrapper, _fn, _i, _len, _ref;
  url = _arg.url, proxy = _arg.proxy;
  req = request.defaults({
    json: true,
    proxy: proxy
  });
  auth = URL.parse(url).auth;
  modifyArgs = function(args) {
    var arg, opts;
    arg = args[0];
    opts = typeof arg === 'string' ? {
      url: arg
    } : arg;
    url = opts.url || opts.uri;
    url = URL.parse(url);
    if (url.auth !== auth) {
      url.host = "" + auth + "@" + url.host;
    }
    url = URL.format(url);
    opts.url = opts.uri = url;
    opts.headers || (opts.headers = {});
    opts.headers['User-Agent'] = USER_AGENT;
    opts.headers['X-Stream'] = true;
    args[0] = opts;
    return args;
  };
  wrapper = {};
  _ref = ['get', 'post', 'put', 'del', 'head'];
  _fn = function(verb) {
    return wrapper[verb] = function() {
      var args;
      args = 1 <= arguments.length ? __slice.call(arguments, 0) : [];
      return req[verb].apply(req, modifyArgs(args));
    };
  };
  for (_i = 0, _len = _ref.length; _i < _len; _i++) {
    verb = _ref[_i];
    _fn(verb);
  }
  return wrapper;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
