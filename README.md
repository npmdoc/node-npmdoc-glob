# npmdoc-glob

#### basic api documentation for  [glob (7.1.2)](https://github.com/isaacs/node-glob#readme)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-glob.svg)](https://travis-ci.org/npmdoc/node-npmdoc-glob)

#### a little globber

[![NPM](https://nodei.co/npm/glob.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/glob)

- [https://npmdoc.github.io/node-npmdoc-glob/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-glob/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-glob/build/screenshot.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-glob/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-glob/build/screenshot.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-glob/build/screenshot.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Isaac Z. Schlueter",
        "url": "http://blog.izs.me/"
    },
    "bugs": {
        "url": "https://github.com/isaacs/node-glob/issues"
    },
    "dependencies": {
        "fs.realpath": "^1.0.0",
        "inflight": "^1.0.4",
        "inherits": "2",
        "minimatch": "^3.0.4",
        "once": "^1.3.0",
        "path-is-absolute": "^1.0.0"
    },
    "description": "a little globber",
    "devDependencies": {
        "mkdirp": "0",
        "rimraf": "^2.2.8",
        "tap": "^7.1.2",
        "tick": "0.0.6"
    },
    "directories": {},
    "dist": {
        "integrity": "sha512-MJTUg1kjuLeQCJ+ccE4Vpa6kKVXkPYJ2mOCQyUuKLcLQsdrMCpBPUi8qVE6+YuaJkozeA9NusTAw3hLr8Xe5EQ==",
        "shasum": "c19c9df9a028702d678612384a6552404c636d15",
        "tarball": "https://registry.npmjs.org/glob/-/glob-7.1.2.tgz"
    },
    "engines": {
        "node": "*"
    },
    "files": [
        "glob.js",
        "sync.js",
        "common.js"
    ],
    "gitHead": "8fa8d561e08c9eed1d286c6a35be2cd8123b2fb7",
    "homepage": "https://github.com/isaacs/node-glob#readme",
    "license": "ISC",
    "main": "glob.js",
    "maintainers": [
        {
            "name": "isaacs"
        }
    ],
    "name": "glob",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/isaacs/node-glob.git"
    },
    "scripts": {
        "bench": "bash benchmark.sh",
        "benchclean": "node benchclean.js",
        "prepublish": "npm run benchclean",
        "prof": "bash prof.sh && cat profile.txt",
        "profclean": "rm -f v8.log profile.txt",
        "test": "tap test/*.js --cov",
        "test-regen": "npm run profclean && TEST_REGEN=1 node test/00-setup.js"
    },
    "version": "7.1.2",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
