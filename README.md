# npmtest-search-index

#### test coverage for  [search-index (v0.10.0)](https://github.com/fergiemcdowall/search-index)  [![npm package](https://img.shields.io/npm/v/npmtest-search-index.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-search-index) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-search-index.svg)](https://travis-ci.org/npmtest/node-npmtest-search-index)

#### A persistent full text search engine for the browser and Node.js

[![NPM](https://nodei.co/npm/search-index.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/search-index)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-search-index/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-search-index/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-search-index/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-search-index/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-search-index/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-search-index/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-search-index/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-search-index/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-search-index/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-search-index/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-search-index/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-search-index/build/test-report.html](https://npmtest.github.io/node-npmtest-search-index/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-search-index/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-search-index/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-search-index/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-search-index/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-search-index/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-search-index/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-search-index/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-search-index/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Fergus McDowall"
    },
    "browser": {
        "leveldown": "level-js"
    },
    "bugs": {
        "url": "https://github.com/fergiemcdowall/search-index/issues"
    },
    "dependencies": {
        "bunyan": "^1.8.10",
        "leveldown": "^1.6.0",
        "levelup": "^1.3.5",
        "search-index-adder": "^0.2.1",
        "search-index-searcher": "^0.2.0"
    },
    "description": "A persistent full text search engine for the browser and Node.js",
    "devDependencies": {
        "JSONStream": "^1.1.4",
        "brfs": "^1.4.3",
        "browser-run": "^3.3.0",
        "browserify": "^13.1.0",
        "disc": "^1.3.2",
        "highland": "^2.10.0",
        "http-server": "^0.9.0",
        "left-pad": "^1.1.3",
        "level-js": "^2.2.4",
        "mocha": "^3.2.0",
        "request": "^2.78.0",
        "reuters-21578-json": "0.0.8",
        "semantic-release": "^6.3.2",
        "semantic-release-cli": "^3.0.3",
        "should": "^10.0.0",
        "sqldown": "^2.1.0",
        "sqlite3": "^3.1.4",
        "standard": "8.1.0",
        "stopword": "^0.1.1",
        "tape": "^4.6.0",
        "term-vector": "0.1.2",
        "uglifyjs": "^2.4.10",
        "written-number": "^0.5.0"
    },
    "directories": {},
    "dist": {
        "shasum": "31c20697b64b6fd37cdb1ea8bcaf86538acacbe5",
        "tarball": "https://registry.npmjs.org/search-index/-/search-index-0.10.0.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "gitHead": "bf6af75377f9dc4d8cafdc7a420d6601aa3bfcd7",
    "homepage": "https://github.com/fergiemcdowall/search-index",
    "keywords": [
        "index",
        "language",
        "lucene",
        "natural",
        "offline",
        "search"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "fergie"
        },
        {
            "name": "mewwts"
        }
    ],
    "name": "search-index",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/fergiemcdowall/search-index.git"
    },
    "scripts": {
        "anylize-web-bundle": "browserify --full-paths lib/index.js --standalone SearchIndex > dist/search-index-full-paths.js && discify dist/search-index-full-paths.js > dist/out.html",
        "demo-server": "http-server && echo 'demo is running at /doc/demo/'",
        "dist": "browserify lib/index.js --standalone SearchIndex > dist/search-index.js",
        "dist-min": "npm run dist && cat dist/search-index.js | uglifyjs -c dead_code > dist/search-index.min.js && cp dist/search-index.min.js docs/demo/",
        "empty-sandbox": "rm -rf test/sandbox && mkdir test/sandbox",
        "semantic-release": "semantic-release pre && npm publish && semantic-release post",
        "test": "npm run empty-sandbox && date && npm run test-node && npm run test-browser && standard test/* lib/*",
        "test-browser": "node test/browser/runtest.js",
        "test-node": "tape test/node/tape-tests/*.js && mocha test/node/mocha-tests --recursive --timeout 10000",
        "test-with-local-deps": "npm install && npm install ../search-index-adder ../search-index-searcher && npm test"
    },
    "version": "0.10.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
