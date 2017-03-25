# api documentation for  [glob (v7.1.1)](https://github.com/isaacs/node-glob#readme)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-glob.svg)](https://travis-ci.org/npmdoc/node-npmdoc-glob)
#### a little globber

[![NPM](https://nodei.co/npm/glob.png?downloads=true)](https://www.npmjs.com/package/glob)

[![apidoc](https://npmdoc.github.io/node-npmdoc-glob/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-glob_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-glob/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-glob/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Isaac Z. Schlueter",
        "email": "i@izs.me",
        "url": "http://blog.izs.me/"
    },
    "bugs": {
        "url": "https://github.com/isaacs/node-glob/issues"
    },
    "dependencies": {
        "fs.realpath": "^1.0.0",
        "inflight": "^1.0.4",
        "inherits": "2",
        "minimatch": "^3.0.2",
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
        "shasum": "805211df04faaf1c63a3600306cdf5ade50b2ec8",
        "tarball": "https://registry.npmjs.org/glob/-/glob-7.1.1.tgz"
    },
    "engines": {
        "node": "*"
    },
    "files": [
        "glob.js",
        "sync.js",
        "common.js"
    ],
    "gitHead": "bc8d43b736a98a9e289fdfceee9266cff35e5742",
    "homepage": "https://github.com/isaacs/node-glob#readme",
    "license": "ISC",
    "main": "glob.js",
    "maintainers": [
        {
            "name": "isaacs",
            "email": "i@izs.me"
        }
    ],
    "name": "glob",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "7.1.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module glob](#apidoc.module.glob)
1.  [function <span class="apidocSignatureSpan"></span>glob (pattern, options, cb)](#apidoc.element.glob.glob)
1.  [function <span class="apidocSignatureSpan">glob.</span>Glob (pattern, options, cb)](#apidoc.element.glob.Glob)
1.  [function <span class="apidocSignatureSpan">glob.</span>GlobSync (pattern, options)](#apidoc.element.glob.GlobSync)
1.  [function <span class="apidocSignatureSpan">glob.</span>hasMagic (pattern, options_)](#apidoc.element.glob.hasMagic)
1.  [function <span class="apidocSignatureSpan">glob.</span>sync (pattern, options)](#apidoc.element.glob.sync)
1.  object <span class="apidocSignatureSpan">glob.</span>Glob.prototype
1.  object <span class="apidocSignatureSpan">glob.</span>GlobSync.prototype

#### [module glob.Glob](#apidoc.module.glob.Glob)
1.  [function <span class="apidocSignatureSpan">glob.</span>Glob (pattern, options, cb)](#apidoc.element.glob.Glob.Glob)
1.  [function <span class="apidocSignatureSpan">glob.Glob.</span>super_ ()](#apidoc.element.glob.Glob.super_)

#### [module glob.Glob.prototype](#apidoc.module.glob.Glob.prototype)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_emitMatch (index, e)](#apidoc.element.glob.Glob.prototype._emitMatch)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_finish ()](#apidoc.element.glob.Glob.prototype._finish)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_makeAbs (f)](#apidoc.element.glob.Glob.prototype._makeAbs)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_mark (p)](#apidoc.element.glob.Glob.prototype._mark)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_process (pattern, index, inGlobStar, cb)](#apidoc.element.glob.Glob.prototype._process)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processGlobStar (prefix, read, abs, remain, index, inGlobStar, cb)](#apidoc.element.glob.Glob.prototype._processGlobStar)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processGlobStar2 (prefix, read, abs, remain, index, inGlobStar, entries, cb)](#apidoc.element.glob.Glob.prototype._processGlobStar2)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processReaddir (prefix, read, abs, remain, index, inGlobStar, cb)](#apidoc.element.glob.Glob.prototype._processReaddir)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processReaddir2 (prefix, read, abs, remain, index, inGlobStar, entries, cb)](#apidoc.element.glob.Glob.prototype._processReaddir2)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processSimple (prefix, index, cb)](#apidoc.element.glob.Glob.prototype._processSimple)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processSimple2 (prefix, index, er, exists, cb)](#apidoc.element.glob.Glob.prototype._processSimple2)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_readdir (abs, inGlobStar, cb)](#apidoc.element.glob.Glob.prototype._readdir)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_readdirEntries (abs, entries, cb)](#apidoc.element.glob.Glob.prototype._readdirEntries)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_readdirError (f, er, cb)](#apidoc.element.glob.Glob.prototype._readdirError)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_readdirInGlobStar (abs, cb)](#apidoc.element.glob.Glob.prototype._readdirInGlobStar)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_realpath ()](#apidoc.element.glob.Glob.prototype._realpath)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_realpathSet (index, cb)](#apidoc.element.glob.Glob.prototype._realpathSet)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_stat (f, cb)](#apidoc.element.glob.Glob.prototype._stat)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_stat2 (f, abs, er, stat, cb)](#apidoc.element.glob.Glob.prototype._stat2)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>abort ()](#apidoc.element.glob.Glob.prototype.abort)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>pause ()](#apidoc.element.glob.Glob.prototype.pause)
1.  [function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>resume ()](#apidoc.element.glob.Glob.prototype.resume)

#### [module glob.GlobSync](#apidoc.module.glob.GlobSync)
1.  [function <span class="apidocSignatureSpan">glob.</span>GlobSync (pattern, options)](#apidoc.element.glob.GlobSync.GlobSync)

#### [module glob.GlobSync.prototype](#apidoc.module.glob.GlobSync.prototype)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_emitMatch (index, e)](#apidoc.element.glob.GlobSync.prototype._emitMatch)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_finish ()](#apidoc.element.glob.GlobSync.prototype._finish)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_makeAbs (f)](#apidoc.element.glob.GlobSync.prototype._makeAbs)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_mark (p)](#apidoc.element.glob.GlobSync.prototype._mark)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_process (pattern, index, inGlobStar)](#apidoc.element.glob.GlobSync.prototype._process)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_processGlobStar (prefix, read, abs, remain, index, inGlobStar)](#apidoc.element.glob.GlobSync.prototype._processGlobStar)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_processReaddir (prefix, read, abs, remain, index, inGlobStar)](#apidoc.element.glob.GlobSync.prototype._processReaddir)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_processSimple (prefix, index)](#apidoc.element.glob.GlobSync.prototype._processSimple)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_readdir (abs, inGlobStar)](#apidoc.element.glob.GlobSync.prototype._readdir)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_readdirEntries (abs, entries)](#apidoc.element.glob.GlobSync.prototype._readdirEntries)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_readdirError (f, er)](#apidoc.element.glob.GlobSync.prototype._readdirError)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_readdirInGlobStar (abs)](#apidoc.element.glob.GlobSync.prototype._readdirInGlobStar)
1.  [function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_stat (f)](#apidoc.element.glob.GlobSync.prototype._stat)

#### [module glob.sync](#apidoc.module.glob.sync)
1.  [function <span class="apidocSignatureSpan">glob.</span>sync (pattern, options)](#apidoc.element.glob.sync.sync)
1.  [function <span class="apidocSignatureSpan">glob.sync.</span>GlobSync (pattern, options)](#apidoc.element.glob.sync.GlobSync)



# <a name="apidoc.module.glob"></a>[module glob](#apidoc.module.glob)

#### <a name="apidoc.element.glob.glob"></a>[function <span class="apidocSignatureSpan"></span>glob (pattern, options, cb)](#apidoc.element.glob.glob)
- description and source-code
```javascript
function glob(pattern, options, cb) {
  if (typeof options === 'function') cb = options, options = {}
  if (!options) options = {}

  if (options.sync) {
    if (cb)
      throw new TypeError('callback provided to sync glob')
    return globSync(pattern, options)
  }

  return new Glob(pattern, options, cb)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.glob.Glob"></a>[function <span class="apidocSignatureSpan">glob.</span>Glob (pattern, options, cb)](#apidoc.element.glob.Glob)
- description and source-code
```javascript
function Glob(pattern, options, cb) {
  if (typeof options === 'function') {
    cb = options
    options = null
  }

  if (options && options.sync) {
    if (cb)
      throw new TypeError('callback provided to sync glob')
    return new GlobSync(pattern, options)
  }

  if (!(this instanceof Glob))
    return new Glob(pattern, options, cb)

  setopts(this, pattern, options)
  this._didRealPath = false

  // process each pattern in the minimatch set
  var n = this.minimatch.set.length

  // The matches are stored as {<filename>: true,...} so that
  // duplicates are automagically pruned.
  // Later, we do an Object.keys() on these.
  // Keep them as a list so we can fill in when nonull is set.
  this.matches = new Array(n)

  if (typeof cb === 'function') {
    cb = once(cb)
    this.on('error', cb)
    this.on('end', function (matches) {
      cb(null, matches)
    })
  }

  var self = this
  var n = this.minimatch.set.length
  this._processing = 0
  this.matches = new Array(n)

  this._emitQueue = []
  this._processQueue = []
  this.paused = false

  if (this.noprocess)
    return this

  if (n === 0)
    return done()

  var sync = true
  for (var i = 0; i < n; i ++) {
    this._process(this.minimatch.set[i], i, false, done)
  }
  sync = false

  function done () {
    --self._processing
    if (self._processing <= 0) {
      if (sync) {
        process.nextTick(function () {
          self._finish()
        })
      } else {
        self._finish()
      }
    }
  }
}
```
- example usage
```shell
...
var Glob = require("glob").Glob
var mg = new Glob(pattern, options, cb)
'''

It's an EventEmitter, and starts walking the filesystem to find matches
immediately.

### new glob.Glob(pattern, [options], [cb])

* 'pattern' '{String}' pattern to search for
* 'options' '{Object}'
* 'cb' '{Function}' Called when an error occurs, or matches are found
* 'err' '{Error | null}'
* 'matches' '{Array<String>}' filenames found matching the pattern
...
```

#### <a name="apidoc.element.glob.GlobSync"></a>[function <span class="apidocSignatureSpan">glob.</span>GlobSync (pattern, options)](#apidoc.element.glob.GlobSync)
- description and source-code
```javascript
function GlobSync(pattern, options) {
  if (!pattern)
    throw new Error('must provide pattern')

  if (typeof options === 'function' || arguments.length === 3)
    throw new TypeError('callback provided to sync glob\n'+
                        'See: https://github.com/isaacs/node-glob/issues/167')

  if (!(this instanceof GlobSync))
    return new GlobSync(pattern, options)

  setopts(this, pattern, options)

  if (this.noprocess)
    return this

  var n = this.minimatch.set.length
  this.matches = new Array(n)
  for (var i = 0; i < n; i ++) {
    this._process(this.minimatch.set[i], i, false)
  }
  this._finish()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.glob.hasMagic"></a>[function <span class="apidocSignatureSpan">glob.</span>hasMagic (pattern, options_)](#apidoc.element.glob.hasMagic)
- description and source-code
```javascript
hasMagic = function (pattern, options_) {
  var options = extend({}, options_)
  options.noprocess = true

  var g = new Glob(pattern, options)
  var set = g.minimatch.set

  if (!pattern)
    return false

  if (set.length > 1)
    return true

  for (var j = 0; j < set[0].length; j++) {
    if (typeof set[0][j] !== 'string')
      return true
  }

  return false
}
```
- example usage
```shell
...

* 'man sh'
* 'man bash' (Search for "Pattern Matching")
* 'man 3 fnmatch'
* 'man 5 gitignore'
* [minimatch documentation](https://github.com/isaacs/minimatch)

## glob.hasMagic(pattern, [options])

Returns 'true' if there are any special characters in the pattern, and
'false' otherwise.

Note that the options affect the results.  If 'noext:true' is set in
the options object, then '+(a|b)' will not be considered a magic
pattern.  If the pattern has a brace expansion, like 'a/{b/c,x/y}'
...
```

#### <a name="apidoc.element.glob.sync"></a>[function <span class="apidocSignatureSpan">glob.</span>sync (pattern, options)](#apidoc.element.glob.sync)
- description and source-code
```javascript
function globSync(pattern, options) {
  if (typeof options === 'function' || arguments.length === 3)
    throw new TypeError('callback provided to sync glob\n'+
                        'See: https://github.com/isaacs/node-glob/issues/167')

  return new GlobSync(pattern, options).found
}
```
- example usage
```shell
...
* 'options' '{Object}'
* 'cb' '{Function}'
  * 'err' '{Error | null}'
  * 'matches' '{Array<String>}' filenames found matching the pattern

Perform an asynchronous glob search.

## glob.sync(pattern, [options])

* 'pattern' '{String}' Pattern to be matched
* 'options' '{Object}'
* return: '{Array<String>}' filenames found matching the pattern

Perform a synchronous glob search.
...
```



# <a name="apidoc.module.glob.Glob"></a>[module glob.Glob](#apidoc.module.glob.Glob)

#### <a name="apidoc.element.glob.Glob.Glob"></a>[function <span class="apidocSignatureSpan">glob.</span>Glob (pattern, options, cb)](#apidoc.element.glob.Glob.Glob)
- description and source-code
```javascript
function Glob(pattern, options, cb) {
  if (typeof options === 'function') {
    cb = options
    options = null
  }

  if (options && options.sync) {
    if (cb)
      throw new TypeError('callback provided to sync glob')
    return new GlobSync(pattern, options)
  }

  if (!(this instanceof Glob))
    return new Glob(pattern, options, cb)

  setopts(this, pattern, options)
  this._didRealPath = false

  // process each pattern in the minimatch set
  var n = this.minimatch.set.length

  // The matches are stored as {<filename>: true,...} so that
  // duplicates are automagically pruned.
  // Later, we do an Object.keys() on these.
  // Keep them as a list so we can fill in when nonull is set.
  this.matches = new Array(n)

  if (typeof cb === 'function') {
    cb = once(cb)
    this.on('error', cb)
    this.on('end', function (matches) {
      cb(null, matches)
    })
  }

  var self = this
  var n = this.minimatch.set.length
  this._processing = 0
  this.matches = new Array(n)

  this._emitQueue = []
  this._processQueue = []
  this.paused = false

  if (this.noprocess)
    return this

  if (n === 0)
    return done()

  var sync = true
  for (var i = 0; i < n; i ++) {
    this._process(this.minimatch.set[i], i, false, done)
  }
  sync = false

  function done () {
    --self._processing
    if (self._processing <= 0) {
      if (sync) {
        process.nextTick(function () {
          self._finish()
        })
      } else {
        self._finish()
      }
    }
  }
}
```
- example usage
```shell
...
var Glob = require("glob").Glob
var mg = new Glob(pattern, options, cb)
'''

It's an EventEmitter, and starts walking the filesystem to find matches
immediately.

### new glob.Glob(pattern, [options], [cb])

* 'pattern' '{String}' pattern to search for
* 'options' '{Object}'
* 'cb' '{Function}' Called when an error occurs, or matches are found
* 'err' '{Error | null}'
* 'matches' '{Array<String>}' filenames found matching the pattern
...
```

#### <a name="apidoc.element.glob.Glob.super_"></a>[function <span class="apidocSignatureSpan">glob.Glob.</span>super_ ()](#apidoc.element.glob.Glob.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.glob.Glob.prototype"></a>[module glob.Glob.prototype](#apidoc.module.glob.Glob.prototype)

#### <a name="apidoc.element.glob.Glob.prototype._emitMatch"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_emitMatch (index, e)](#apidoc.element.glob.Glob.prototype._emitMatch)
- description and source-code
```javascript
_emitMatch = function (index, e) {
  if (this.aborted)
    return

  if (isIgnored(this, e))
    return

  if (this.paused) {
    this._emitQueue.push([index, e])
    return
  }

  var abs = isAbsolute(e) ? e : this._makeAbs(e)

  if (this.mark)
    e = this._mark(e)

  if (this.absolute)
    e = abs

  if (this.matches[index][e])
    return

  if (this.nodir) {
    var c = this.cache[abs]
    if (c === 'DIR' || Array.isArray(c))
      return
  }

  this.matches[index][e] = true

  var st = this.statCache[abs]
  if (st)
    this.emit('stat', e, st)

  this.emit('match', e)
}
```
- example usage
```shell
...
this.emit('resume')
this.paused = false
if (this._emitQueue.length) {
  var eq = this._emitQueue.slice(0)
  this._emitQueue.length = 0
  for (var i = 0; i < eq.length; i ++) {
    var e = eq[i]
    this._emitMatch(e[0], e[1])
  }
}
if (this._processQueue.length) {
  var pq = this._processQueue.slice(0)
  this._processQueue.length = 0
  for (var i = 0; i < pq.length; i ++) {
    var p = pq[i]
...
```

#### <a name="apidoc.element.glob.Glob.prototype._finish"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_finish ()](#apidoc.element.glob.Glob.prototype._finish)
- description and source-code
```javascript
_finish = function () {
  assert(this instanceof Glob)
  if (this.aborted)
    return

  if (this.realpath && !this._didRealpath)
    return this._realpath()

  common.finish(this)
  this.emit('end', this.found)
}
```
- example usage
```shell
...
  sync = false

  function done () {
    --self._processing
    if (self._processing <= 0) {
      if (sync) {
        process.nextTick(function () {
          self._finish()
        })
      } else {
        self._finish()
      }
    }
  }
}
...
```

#### <a name="apidoc.element.glob.Glob.prototype._makeAbs"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_makeAbs (f)](#apidoc.element.glob.Glob.prototype._makeAbs)
- description and source-code
```javascript
_makeAbs = function (f) {
  return common.makeAbs(this, f)
}
```
- example usage
```shell
...
  return cb()

var set = this.matches[index] = Object.create(null)
found.forEach(function (p, i) {
  // If there's a problem with the stat, then it means that
  // one or more of the links in the realpath couldn't be
  // resolved.  just return the abs value in that case.
  p = self._makeAbs(p)
  rp.realpath(p, self.realpathCache, function (er, real) {
    if (!er)
      set[real] = true
    else if (er.syscall === 'stat')
      set[p] = true
    else
      self.emit('error', er) // srsly wtf right here
...
```

#### <a name="apidoc.element.glob.Glob.prototype._mark"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_mark (p)](#apidoc.element.glob.Glob.prototype._mark)
- description and source-code
```javascript
_mark = function (p) {
  return common.mark(this, p)
}
```
- example usage
```shell
...
  this._emitQueue.push([index, e])
  return
}

var abs = isAbsolute(e) ? e : this._makeAbs(e)

if (this.mark)
  e = this._mark(e)

if (this.absolute)
  e = abs

if (this.matches[index][e])
  return
...
```

#### <a name="apidoc.element.glob.Glob.prototype._process"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_process (pattern, index, inGlobStar, cb)](#apidoc.element.glob.Glob.prototype._process)
- description and source-code
```javascript
_process = function (pattern, index, inGlobStar, cb) {
  assert(this instanceof Glob)
  assert(typeof cb === 'function')

  if (this.aborted)
    return

  this._processing++
  if (this.paused) {
    this._processQueue.push([pattern, index, inGlobStar, cb])
    return
  }

  //console.error('PROCESS %d', this._processing, pattern)

  // Get the first [n] parts of pattern that are all strings.
  var n = 0
  while (typeof pattern[n] === 'string') {
    n ++
  }
  // now n is the index of the first one that is *not* a string.

  // see if there's anything else
  var prefix
  switch (n) {
    // if not, then this is rather simple
    case pattern.length:
      this._processSimple(pattern.join('/'), index, cb)
      return

    case 0:
      // pattern *starts* with some non-trivial item.
      // going to readdir(cwd), but not include the prefix in matches.
      prefix = null
      break

    default:
      // pattern has some string bits in the front.
      // whatever it starts with, whether that's 'absolute' like /foo/bar,
      // or 'relative' like '../baz'
      prefix = pattern.slice(0, n).join('/')
      break
  }

  var remain = pattern.slice(n)

  // get the list of entries.
  var read
  if (prefix === null)
    read = '.'
  else if (isAbsolute(prefix) || isAbsolute(pattern.join('/'))) {
    if (!prefix || !isAbsolute(prefix))
      prefix = '/' + prefix
    read = prefix
  } else
    read = prefix

  var abs = this._makeAbs(read)

  //if ignored, skip _processing
  if (childrenIgnored(this, read))
    return cb()

  var isGlobStar = remain[0] === minimatch.GLOBSTAR
  if (isGlobStar)
    this._processGlobStar(prefix, read, abs, remain, index, inGlobStar, cb)
  else
    this._processReaddir(prefix, read, abs, remain, index, inGlobStar, cb)
}
```
- example usage
```shell
...
  return this

if (n === 0)
  return done()

var sync = true
for (var i = 0; i < n; i ++) {
  this._process(this.minimatch.set[i], i, false, done)
}
sync = false

function done () {
  --self._processing
  if (self._processing <= 0) {
    if (sync) {
...
```

#### <a name="apidoc.element.glob.Glob.prototype._processGlobStar"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processGlobStar (prefix, read, abs, remain, index, inGlobStar, cb)](#apidoc.element.glob.Glob.prototype._processGlobStar)
- description and source-code
```javascript
_processGlobStar = function (prefix, read, abs, remain, index, inGlobStar, cb) {
  var self = this
  this._readdir(abs, inGlobStar, function (er, entries) {
    self._processGlobStar2(prefix, read, abs, remain, index, inGlobStar, entries, cb)
  })
}
```
- example usage
```shell
...

//if ignored, skip _processing
if (childrenIgnored(this, read))
  return cb()

var isGlobStar = remain[0] === minimatch.GLOBSTAR
if (isGlobStar)
  this._processGlobStar(prefix, read, abs, remain, index, inGlobStar, cb)
else
  this._processReaddir(prefix, read, abs, remain, index, inGlobStar, cb)
}

Glob.prototype._processReaddir = function (prefix, read, abs, remain, index, inGlobStar, cb) {
var self = this
this._readdir(abs, inGlobStar, function (er, entries) {
...
```

#### <a name="apidoc.element.glob.Glob.prototype._processGlobStar2"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processGlobStar2 (prefix, read, abs, remain, index, inGlobStar, entries, cb)](#apidoc.element.glob.Glob.prototype._processGlobStar2)
- description and source-code
```javascript
_processGlobStar2 = function (prefix, read, abs, remain, index, inGlobStar, entries, cb) {
  //console.error('pgs2', prefix, remain[0], entries)

  // no entries means not a dir, so it can never have matches
  // foo.txt/** doesn't match foo.txt
  if (!entries)
    return cb()

  // test without the globstar, and with every child both below
  // and replacing the globstar.
  var remainWithoutGlobStar = remain.slice(1)
  var gspref = prefix ? [ prefix ] : []
  var noGlobStar = gspref.concat(remainWithoutGlobStar)

  // the noGlobStar pattern exits the inGlobStar state
  this._process(noGlobStar, index, false, cb)

  var isSym = this.symlinks[abs]
  var len = entries.length

  // If it's a symlink, and we're in a globstar, then stop
  if (isSym && inGlobStar)
    return cb()

  for (var i = 0; i < len; i++) {
    var e = entries[i]
    if (e.charAt(0) === '.' && !this.dot)
      continue

    // these two cases enter the inGlobStar state
    var instead = gspref.concat(entries[i], remainWithoutGlobStar)
    this._process(instead, index, true, cb)

    var below = gspref.concat(entries[i], remain)
    this._process(below, index, true, cb)
  }

  cb()
}
```
- example usage
```shell
...

return cb()
}

Glob.prototype._processGlobStar = function (prefix, read, abs, remain, index, inGlobStar, cb) {
var self = this
this._readdir(abs, inGlobStar, function (er, entries) {
  self._processGlobStar2(prefix, read, abs, remain, index, inGlobStar, entries, cb)
})
}


Glob.prototype._processGlobStar2 = function (prefix, read, abs, remain, index, inGlobStar, entries, cb) {
//console.error('pgs2', prefix, remain[0], entries)
...
```

#### <a name="apidoc.element.glob.Glob.prototype._processReaddir"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processReaddir (prefix, read, abs, remain, index, inGlobStar, cb)](#apidoc.element.glob.Glob.prototype._processReaddir)
- description and source-code
```javascript
_processReaddir = function (prefix, read, abs, remain, index, inGlobStar, cb) {
  var self = this
  this._readdir(abs, inGlobStar, function (er, entries) {
    return self._processReaddir2(prefix, read, abs, remain, index, inGlobStar, entries, cb)
  })
}
```
- example usage
```shell
...
if (childrenIgnored(this, read))
  return cb()

var isGlobStar = remain[0] === minimatch.GLOBSTAR
if (isGlobStar)
  this._processGlobStar(prefix, read, abs, remain, index, inGlobStar, cb)
else
  this._processReaddir(prefix, read, abs, remain, index, inGlobStar, cb)
}

Glob.prototype._processReaddir = function (prefix, read, abs, remain, index, inGlobStar, cb) {
var self = this
this._readdir(abs, inGlobStar, function (er, entries) {
  return self._processReaddir2(prefix, read, abs, remain, index, inGlobStar, entries, cb)
})
...
```

#### <a name="apidoc.element.glob.Glob.prototype._processReaddir2"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processReaddir2 (prefix, read, abs, remain, index, inGlobStar, entries, cb)](#apidoc.element.glob.Glob.prototype._processReaddir2)
- description and source-code
```javascript
_processReaddir2 = function (prefix, read, abs, remain, index, inGlobStar, entries, cb) {

  // if the abs isn't a dir, then nothing can match!
  if (!entries)
    return cb()

  // It will only match dot entries if it starts with a dot, or if
  // dot is set.  Stuff like @(.foo|.bar) isn't allowed.
  var pn = remain[0]
  var negate = !!this.minimatch.negate
  var rawGlob = pn._glob
  var dotOk = this.dot || rawGlob.charAt(0) === '.'

  var matchedEntries = []
  for (var i = 0; i < entries.length; i++) {
    var e = entries[i]
    if (e.charAt(0) !== '.' || dotOk) {
      var m
      if (negate && !prefix) {
        m = !e.match(pn)
      } else {
        m = e.match(pn)
      }
      if (m)
        matchedEntries.push(e)
    }
  }

  //console.error('prd2', prefix, entries, remain[0]._glob, matchedEntries)

  var len = matchedEntries.length
  // If there are no matched entries, then nothing matches.
  if (len === 0)
    return cb()

  // if this is the last remaining pattern bit, then no need for
  // an additional stat *unless* the user has specified mark or
  // stat explicitly.  We know they exist, since readdir returned
  // them.

  if (remain.length === 1 && !this.mark && !this.stat) {
    if (!this.matches[index])
      this.matches[index] = Object.create(null)

    for (var i = 0; i < len; i ++) {
      var e = matchedEntries[i]
      if (prefix) {
        if (prefix !== '/')
          e = prefix + '/' + e
        else
          e = prefix + e
      }

      if (e.charAt(0) === '/' && !this.nomount) {
        e = path.join(this.root, e)
      }
      this._emitMatch(index, e)
    }
    // This was the last one, and no stats were needed
    return cb()
  }

  // now test all matched entries as stand-ins for that part
  // of the pattern.
  remain.shift()
  for (var i = 0; i < len; i ++) {
    var e = matchedEntries[i]
    var newPattern
    if (prefix) {
      if (prefix !== '/')
        e = prefix + '/' + e
      else
        e = prefix + e
    }
    this._process([e].concat(remain), index, inGlobStar, cb)
  }
  cb()
}
```
- example usage
```shell
...
else
  this._processReaddir(prefix, read, abs, remain, index, inGlobStar, cb)
}

Glob.prototype._processReaddir = function (prefix, read, abs, remain, index, inGlobStar, cb) {
var self = this
this._readdir(abs, inGlobStar, function (er, entries) {
  return self._processReaddir2(prefix, read, abs, remain, index, inGlobStar, entries, cb)
})
}

Glob.prototype._processReaddir2 = function (prefix, read, abs, remain, index, inGlobStar, entries, cb) {

// if the abs isn't a dir, then nothing can match!
if (!entries)
...
```

#### <a name="apidoc.element.glob.Glob.prototype._processSimple"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processSimple (prefix, index, cb)](#apidoc.element.glob.Glob.prototype._processSimple)
- description and source-code
```javascript
_processSimple = function (prefix, index, cb) {
  // XXX review this.  Shouldn't it be doing the mounting etc
  // before doing stat?  kinda weird?
  var self = this
  this._stat(prefix, function (er, exists) {
    self._processSimple2(prefix, index, er, exists, cb)
  })
}
```
- example usage
```shell
...
  // now n is the index of the first one that is *not* a string.

  // see if there's anything else
  var prefix
  switch (n) {
// if not, then this is rather simple
case pattern.length:
  this._processSimple(pattern.join('/'), index, cb)
  return

case 0:
  // pattern *starts* with some non-trivial item.
  // going to readdir(cwd), but not include the prefix in matches.
  prefix = null
  break
...
```

#### <a name="apidoc.element.glob.Glob.prototype._processSimple2"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_processSimple2 (prefix, index, er, exists, cb)](#apidoc.element.glob.Glob.prototype._processSimple2)
- description and source-code
```javascript
_processSimple2 = function (prefix, index, er, exists, cb) {

  //console.error('ps2', prefix, exists)

  if (!this.matches[index])
    this.matches[index] = Object.create(null)

  // If it doesn't exist, then just mark the lack of results
  if (!exists)
    return cb()

  if (prefix && isAbsolute(prefix) && !this.nomount) {
    var trail = /[\/\\]$/.test(prefix)
    if (prefix.charAt(0) === '/') {
      prefix = path.join(this.root, prefix)
    } else {
      prefix = path.resolve(this.root, prefix)
      if (trail)
        prefix += '/'
    }
  }

  if (process.platform === 'win32')
    prefix = prefix.replace(/\\/g, '/')

  // Mark this as a match
  this._emitMatch(index, prefix)
  cb()
}
```
- example usage
```shell
...
}

Glob.prototype._processSimple = function (prefix, index, cb) {
// XXX review this.  Shouldn't it be doing the mounting etc
// before doing stat?  kinda weird?
var self = this
this._stat(prefix, function (er, exists) {
  self._processSimple2(prefix, index, er, exists, cb)
})
}
Glob.prototype._processSimple2 = function (prefix, index, er, exists, cb) {

//console.error('ps2', prefix, exists)

if (!this.matches[index])
...
```

#### <a name="apidoc.element.glob.Glob.prototype._readdir"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_readdir (abs, inGlobStar, cb)](#apidoc.element.glob.Glob.prototype._readdir)
- description and source-code
```javascript
_readdir = function (abs, inGlobStar, cb) {
  if (this.aborted)
    return

  cb = inflight('readdir\0'+abs+'\0'+inGlobStar, cb)
  if (!cb)
    return

  //console.error('RD %j %j', +inGlobStar, abs)
  if (inGlobStar && !ownProp(this.symlinks, abs))
    return this._readdirInGlobStar(abs, cb)

  if (ownProp(this.cache, abs)) {
    var c = this.cache[abs]
    if (!c || c === 'FILE')
      return cb()

    if (Array.isArray(c))
      return cb(null, c)
  }

  var self = this
  fs.readdir(abs, readdirCb(this, abs, cb))
}
```
- example usage
```shell
...
  this._processGlobStar(prefix, read, abs, remain, index, inGlobStar, cb)
else
  this._processReaddir(prefix, read, abs, remain, index, inGlobStar, cb)
}

Glob.prototype._processReaddir = function (prefix, read, abs, remain, index, inGlobStar, cb) {
var self = this
this._readdir(abs, inGlobStar, function (er, entries) {
  return self._processReaddir2(prefix, read, abs, remain, index, inGlobStar, entries, cb)
})
}

Glob.prototype._processReaddir2 = function (prefix, read, abs, remain, index, inGlobStar, entries, cb) {

// if the abs isn't a dir, then nothing can match!
...
```

#### <a name="apidoc.element.glob.Glob.prototype._readdirEntries"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_readdirEntries (abs, entries, cb)](#apidoc.element.glob.Glob.prototype._readdirEntries)
- description and source-code
```javascript
_readdirEntries = function (abs, entries, cb) {
  if (this.aborted)
    return

  // if we haven't asked to stat everything, then just
  // assume that everything in there exists, so we can avoid
  // having to stat it a second time.
  if (!this.mark && !this.stat) {
    for (var i = 0; i < entries.length; i ++) {
      var e = entries[i]
      if (abs === '/')
        e = abs + e
      else
        e = abs + '/' + e
      this.cache[e] = true
    }
  }

  this.cache[abs] = entries
  return cb(null, entries)
}
```
- example usage
```shell
...
}

function readdirCb (self, abs, cb) {
return function (er, entries) {
  if (er)
    self._readdirError(abs, er, cb)
  else
    self._readdirEntries(abs, entries, cb)
}
}

Glob.prototype._readdirEntries = function (abs, entries, cb) {
if (this.aborted)
  return
...
```

#### <a name="apidoc.element.glob.Glob.prototype._readdirError"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_readdirError (f, er, cb)](#apidoc.element.glob.Glob.prototype._readdirError)
- description and source-code
```javascript
_readdirError = function (f, er, cb) {
  if (this.aborted)
    return

  // handle errors, and cache the information
  switch (er.code) {
    case 'ENOTSUP': // https://github.com/isaacs/node-glob/issues/205
    case 'ENOTDIR': // totally normal. means it *does* exist.
      var abs = this._makeAbs(f)
      this.cache[abs] = 'FILE'
      if (abs === this.cwdAbs) {
        var error = new Error(er.code + ' invalid cwd ' + this.cwd)
        error.path = this.cwd
        error.code = er.code
        this.emit('error', error)
        this.abort()
      }
      break

    case 'ENOENT': // not terribly unusual
    case 'ELOOP':
    case 'ENAMETOOLONG':
    case 'UNKNOWN':
      this.cache[this._makeAbs(f)] = false
      break

    default: // some unusual error.  Treat as failure.
      this.cache[this._makeAbs(f)] = false
      if (this.strict) {
        this.emit('error', er)
        // If the error is handled, then we abort
        // if not, we threw out of here
        this.abort()
      }
      if (!this.silent)
        console.error('glob error', er)
      break
  }

  return cb()
}
```
- example usage
```shell
...
var self = this
fs.readdir(abs, readdirCb(this, abs, cb))
}

function readdirCb (self, abs, cb) {
return function (er, entries) {
  if (er)
    self._readdirError(abs, er, cb)
  else
    self._readdirEntries(abs, entries, cb)
}
}

Glob.prototype._readdirEntries = function (abs, entries, cb) {
if (this.aborted)
...
```

#### <a name="apidoc.element.glob.Glob.prototype._readdirInGlobStar"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_readdirInGlobStar (abs, cb)](#apidoc.element.glob.Glob.prototype._readdirInGlobStar)
- description and source-code
```javascript
_readdirInGlobStar = function (abs, cb) {
  if (this.aborted)
    return

  // follow all symlinked directories forever
  // just proceed as if this is a non-globstar situation
  if (this.follow)
    return this._readdir(abs, false, cb)

  var lstatkey = 'lstat\0' + abs
  var self = this
  var lstatcb = inflight(lstatkey, lstatcb_)

  if (lstatcb)
    fs.lstat(abs, lstatcb)

  function lstatcb_ (er, lstat) {
    if (er && er.code === 'ENOENT')
      return cb()

    var isSym = lstat && lstat.isSymbolicLink()
    self.symlinks[abs] = isSym

    // If it's not a symlink or a dir, then it's definitely a regular file.
    // don't bother doing a readdir in that case.
    if (!isSym && lstat && !lstat.isDirectory()) {
      self.cache[abs] = 'FILE'
      cb()
    } else
      self._readdir(abs, false, cb)
  }
}
```
- example usage
```shell
...

  cb = inflight('readdir\0'+abs+'\0'+inGlobStar, cb)
  if (!cb)
return

  //console.error('RD %j %j', +inGlobStar, abs)
  if (inGlobStar && !ownProp(this.symlinks, abs))
return this._readdirInGlobStar(abs, cb)

  if (ownProp(this.cache, abs)) {
var c = this.cache[abs]
if (!c || c === 'FILE')
  return cb()

if (Array.isArray(c))
...
```

#### <a name="apidoc.element.glob.Glob.prototype._realpath"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_realpath ()](#apidoc.element.glob.Glob.prototype._realpath)
- description and source-code
```javascript
_realpath = function () {
  if (this._didRealpath)
    return

  this._didRealpath = true

  var n = this.matches.length
  if (n === 0)
    return this._finish()

  var self = this
  for (var i = 0; i < this.matches.length; i++)
    this._realpathSet(i, next)

  function next () {
    if (--n === 0)
      self._finish()
  }
}
```
- example usage
```shell
...

Glob.prototype._finish = function () {
assert(this instanceof Glob)
if (this.aborted)
  return

if (this.realpath && !this._didRealpath)
  return this._realpath()

common.finish(this)
this.emit('end', this.found)
}

Glob.prototype._realpath = function () {
if (this._didRealpath)
...
```

#### <a name="apidoc.element.glob.Glob.prototype._realpathSet"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_realpathSet (index, cb)](#apidoc.element.glob.Glob.prototype._realpathSet)
- description and source-code
```javascript
_realpathSet = function (index, cb) {
  var matchset = this.matches[index]
  if (!matchset)
    return cb()

  var found = Object.keys(matchset)
  var self = this
  var n = found.length

  if (n === 0)
    return cb()

  var set = this.matches[index] = Object.create(null)
  found.forEach(function (p, i) {
    // If there's a problem with the stat, then it means that
    // one or more of the links in the realpath couldn't be
    // resolved.  just return the abs value in that case.
    p = self._makeAbs(p)
    rp.realpath(p, self.realpathCache, function (er, real) {
      if (!er)
        set[real] = true
      else if (er.syscall === 'stat')
        set[p] = true
      else
        self.emit('error', er) // srsly wtf right here

      if (--n === 0) {
        self.matches[index] = set
        cb()
      }
    })
  })
}
```
- example usage
```shell
...

  var n = this.matches.length
  if (n === 0)
    return this._finish()

  var self = this
  for (var i = 0; i < this.matches.length; i++)
    this._realpathSet(i, next)

  function next () {
    if (--n === 0)
      self._finish()
  }
}
...
```

#### <a name="apidoc.element.glob.Glob.prototype._stat"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_stat (f, cb)](#apidoc.element.glob.Glob.prototype._stat)
- description and source-code
```javascript
_stat = function (f, cb) {
  var abs = this._makeAbs(f)
  var needDir = f.slice(-1) === '/'

  if (f.length > this.maxLength)
    return cb()

  if (!this.stat && ownProp(this.cache, abs)) {
    var c = this.cache[abs]

    if (Array.isArray(c))
      c = 'DIR'

    // It exists, but maybe not how we need it
    if (!needDir || c === 'DIR')
      return cb(null, c)

    if (needDir && c === 'FILE')
      return cb()

    // otherwise we have to stat, because maybe c=true
    // if we know it exists, but not what it is.
  }

  var exists
  var stat = this.statCache[abs]
  if (stat !== undefined) {
    if (stat === false)
      return cb(null, stat)
    else {
      var type = stat.isDirectory() ? 'DIR' : 'FILE'
      if (needDir && type === 'FILE')
        return cb()
      else
        return cb(null, type, stat)
    }
  }

  var self = this
  var statcb = inflight('stat\0' + abs, lstatcb_)
  if (statcb)
    fs.lstat(abs, statcb)

  function lstatcb_ (er, lstat) {
    if (lstat && lstat.isSymbolicLink()) {
      // If it's a symlink, then treat it as the target, unless
      // the target does not exist, then treat it as a file.
      return fs.stat(abs, function (er, stat) {
        if (er)
          self._stat2(f, abs, null, lstat, cb)
        else
          self._stat2(f, abs, er, stat, cb)
      })
    } else {
      self._stat2(f, abs, er, lstat, cb)
    }
  }
}
```
- example usage
```shell
...
cb()
}

Glob.prototype._processSimple = function (prefix, index, cb) {
// XXX review this.  Shouldn't it be doing the mounting etc
// before doing stat?  kinda weird?
var self = this
this._stat(prefix, function (er, exists) {
  self._processSimple2(prefix, index, er, exists, cb)
})
}
Glob.prototype._processSimple2 = function (prefix, index, er, exists, cb) {

//console.error('ps2', prefix, exists)
...
```

#### <a name="apidoc.element.glob.Glob.prototype._stat2"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>_stat2 (f, abs, er, stat, cb)](#apidoc.element.glob.Glob.prototype._stat2)
- description and source-code
```javascript
_stat2 = function (f, abs, er, stat, cb) {
  if (er && (er.code === 'ENOENT' || er.code === 'ENOTDIR')) {
    this.statCache[abs] = false
    return cb()
  }

  var needDir = f.slice(-1) === '/'
  this.statCache[abs] = stat

  if (abs.slice(-1) === '/' && stat && !stat.isDirectory())
    return cb(null, false, stat)

  var c = true
  if (stat)
    c = stat.isDirectory() ? 'DIR' : 'FILE'
  this.cache[abs] = this.cache[abs] || c

  if (needDir && c === 'FILE')
    return cb()

  return cb(null, c, stat)
}
```
- example usage
```shell
...

function lstatcb_ (er, lstat) {
  if (lstat && lstat.isSymbolicLink()) {
    // If it's a symlink, then treat it as the target, unless
    // the target does not exist, then treat it as a file.
    return fs.stat(abs, function (er, stat) {
      if (er)
        self._stat2(f, abs, null, lstat, cb)
      else
        self._stat2(f, abs, er, stat, cb)
    })
  } else {
    self._stat2(f, abs, er, lstat, cb)
  }
}
...
```

#### <a name="apidoc.element.glob.Glob.prototype.abort"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>abort ()](#apidoc.element.glob.Glob.prototype.abort)
- description and source-code
```javascript
abort = function () {
  this.aborted = true
  this.emit('abort')
}
```
- example usage
```shell
...
  var abs = this._makeAbs(f)
  this.cache[abs] = 'FILE'
  if (abs === this.cwdAbs) {
    var error = new Error(er.code + ' invalid cwd ' + this.cwd)
    error.path = this.cwd
    error.code = er.code
    this.emit('error', error)
    this.abort()
  }
  break

case 'ENOENT': // not terribly unusual
case 'ELOOP':
case 'ENAMETOOLONG':
case 'UNKNOWN':
...
```

#### <a name="apidoc.element.glob.Glob.prototype.pause"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>pause ()](#apidoc.element.glob.Glob.prototype.pause)
- description and source-code
```javascript
pause = function () {
  if (!this.paused) {
    this.paused = true
    this.emit('pause')
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.glob.Glob.prototype.resume"></a>[function <span class="apidocSignatureSpan">glob.Glob.prototype.</span>resume ()](#apidoc.element.glob.Glob.prototype.resume)
- description and source-code
```javascript
resume = function () {
  if (this.paused) {
    this.emit('resume')
    this.paused = false
    if (this._emitQueue.length) {
      var eq = this._emitQueue.slice(0)
      this._emitQueue.length = 0
      for (var i = 0; i < eq.length; i ++) {
        var e = eq[i]
        this._emitMatch(e[0], e[1])
      }
    }
    if (this._processQueue.length) {
      var pq = this._processQueue.slice(0)
      this._processQueue.length = 0
      for (var i = 0; i < pq.length; i ++) {
        var p = pq[i]
        this._processing--
        this._process(p[0], p[1], p[2], p[3])
      }
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.glob.GlobSync"></a>[module glob.GlobSync](#apidoc.module.glob.GlobSync)

#### <a name="apidoc.element.glob.GlobSync.GlobSync"></a>[function <span class="apidocSignatureSpan">glob.</span>GlobSync (pattern, options)](#apidoc.element.glob.GlobSync.GlobSync)
- description and source-code
```javascript
function GlobSync(pattern, options) {
  if (!pattern)
    throw new Error('must provide pattern')

  if (typeof options === 'function' || arguments.length === 3)
    throw new TypeError('callback provided to sync glob\n'+
                        'See: https://github.com/isaacs/node-glob/issues/167')

  if (!(this instanceof GlobSync))
    return new GlobSync(pattern, options)

  setopts(this, pattern, options)

  if (this.noprocess)
    return this

  var n = this.minimatch.set.length
  this.matches = new Array(n)
  for (var i = 0; i < n; i ++) {
    this._process(this.minimatch.set[i], i, false)
  }
  this._finish()
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.glob.GlobSync.prototype"></a>[module glob.GlobSync.prototype](#apidoc.module.glob.GlobSync.prototype)

#### <a name="apidoc.element.glob.GlobSync.prototype._emitMatch"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_emitMatch (index, e)](#apidoc.element.glob.GlobSync.prototype._emitMatch)
- description and source-code
```javascript
_emitMatch = function (index, e) {
  if (isIgnored(this, e))
    return

  var abs = this._makeAbs(e)

  if (this.mark)
    e = this._mark(e)

  if (this.absolute) {
    e = abs
  }

  if (this.matches[index][e])
    return

  if (this.nodir) {
    var c = this.cache[abs]
    if (c === 'DIR' || Array.isArray(c))
      return
  }

  this.matches[index][e] = true

  if (this.stat)
    this._stat(e)
}
```
- example usage
```shell
...
this.emit('resume')
this.paused = false
if (this._emitQueue.length) {
  var eq = this._emitQueue.slice(0)
  this._emitQueue.length = 0
  for (var i = 0; i < eq.length; i ++) {
    var e = eq[i]
    this._emitMatch(e[0], e[1])
  }
}
if (this._processQueue.length) {
  var pq = this._processQueue.slice(0)
  this._processQueue.length = 0
  for (var i = 0; i < pq.length; i ++) {
    var p = pq[i]
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._finish"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_finish ()](#apidoc.element.glob.GlobSync.prototype._finish)
- description and source-code
```javascript
_finish = function () {
  assert(this instanceof GlobSync)
  if (this.realpath) {
    var self = this
    this.matches.forEach(function (matchset, index) {
      var set = self.matches[index] = Object.create(null)
      for (var p in matchset) {
        try {
          p = self._makeAbs(p)
          var real = rp.realpathSync(p, self.realpathCache)
          set[real] = true
        } catch (er) {
          if (er.syscall === 'stat')
            set[self._makeAbs(p)] = true
          else
            throw er
        }
      }
    })
  }
  common.finish(this)
}
```
- example usage
```shell
...
  sync = false

  function done () {
    --self._processing
    if (self._processing <= 0) {
      if (sync) {
        process.nextTick(function () {
          self._finish()
        })
      } else {
        self._finish()
      }
    }
  }
}
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._makeAbs"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_makeAbs (f)](#apidoc.element.glob.GlobSync.prototype._makeAbs)
- description and source-code
```javascript
_makeAbs = function (f) {
  return common.makeAbs(this, f)
}
```
- example usage
```shell
...
  return cb()

var set = this.matches[index] = Object.create(null)
found.forEach(function (p, i) {
  // If there's a problem with the stat, then it means that
  // one or more of the links in the realpath couldn't be
  // resolved.  just return the abs value in that case.
  p = self._makeAbs(p)
  rp.realpath(p, self.realpathCache, function (er, real) {
    if (!er)
      set[real] = true
    else if (er.syscall === 'stat')
      set[p] = true
    else
      self.emit('error', er) // srsly wtf right here
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._mark"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_mark (p)](#apidoc.element.glob.GlobSync.prototype._mark)
- description and source-code
```javascript
_mark = function (p) {
  return common.mark(this, p)
}
```
- example usage
```shell
...
  this._emitQueue.push([index, e])
  return
}

var abs = isAbsolute(e) ? e : this._makeAbs(e)

if (this.mark)
  e = this._mark(e)

if (this.absolute)
  e = abs

if (this.matches[index][e])
  return
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._process"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_process (pattern, index, inGlobStar)](#apidoc.element.glob.GlobSync.prototype._process)
- description and source-code
```javascript
_process = function (pattern, index, inGlobStar) {
  assert(this instanceof GlobSync)

  // Get the first [n] parts of pattern that are all strings.
  var n = 0
  while (typeof pattern[n] === 'string') {
    n ++
  }
  // now n is the index of the first one that is *not* a string.

  // See if there's anything else
  var prefix
  switch (n) {
    // if not, then this is rather simple
    case pattern.length:
      this._processSimple(pattern.join('/'), index)
      return

    case 0:
      // pattern *starts* with some non-trivial item.
      // going to readdir(cwd), but not include the prefix in matches.
      prefix = null
      break

    default:
      // pattern has some string bits in the front.
      // whatever it starts with, whether that's 'absolute' like /foo/bar,
      // or 'relative' like '../baz'
      prefix = pattern.slice(0, n).join('/')
      break
  }

  var remain = pattern.slice(n)

  // get the list of entries.
  var read
  if (prefix === null)
    read = '.'
  else if (isAbsolute(prefix) || isAbsolute(pattern.join('/'))) {
    if (!prefix || !isAbsolute(prefix))
      prefix = '/' + prefix
    read = prefix
  } else
    read = prefix

  var abs = this._makeAbs(read)

  //if ignored, skip processing
  if (childrenIgnored(this, read))
    return

  var isGlobStar = remain[0] === minimatch.GLOBSTAR
  if (isGlobStar)
    this._processGlobStar(prefix, read, abs, remain, index, inGlobStar)
  else
    this._processReaddir(prefix, read, abs, remain, index, inGlobStar)
}
```
- example usage
```shell
...
  return this

if (n === 0)
  return done()

var sync = true
for (var i = 0; i < n; i ++) {
  this._process(this.minimatch.set[i], i, false, done)
}
sync = false

function done () {
  --self._processing
  if (self._processing <= 0) {
    if (sync) {
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._processGlobStar"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_processGlobStar (prefix, read, abs, remain, index, inGlobStar)](#apidoc.element.glob.GlobSync.prototype._processGlobStar)
- description and source-code
```javascript
_processGlobStar = function (prefix, read, abs, remain, index, inGlobStar) {

  var entries = this._readdir(abs, inGlobStar)

  // no entries means not a dir, so it can never have matches
  // foo.txt/** doesn't match foo.txt
  if (!entries)
    return

  // test without the globstar, and with every child both below
  // and replacing the globstar.
  var remainWithoutGlobStar = remain.slice(1)
  var gspref = prefix ? [ prefix ] : []
  var noGlobStar = gspref.concat(remainWithoutGlobStar)

  // the noGlobStar pattern exits the inGlobStar state
  this._process(noGlobStar, index, false)

  var len = entries.length
  var isSym = this.symlinks[abs]

  // If it's a symlink, and we're in a globstar, then stop
  if (isSym && inGlobStar)
    return

  for (var i = 0; i < len; i++) {
    var e = entries[i]
    if (e.charAt(0) === '.' && !this.dot)
      continue

    // these two cases enter the inGlobStar state
    var instead = gspref.concat(entries[i], remainWithoutGlobStar)
    this._process(instead, index, true)

    var below = gspref.concat(entries[i], remain)
    this._process(below, index, true)
  }
}
```
- example usage
```shell
...

//if ignored, skip _processing
if (childrenIgnored(this, read))
  return cb()

var isGlobStar = remain[0] === minimatch.GLOBSTAR
if (isGlobStar)
  this._processGlobStar(prefix, read, abs, remain, index, inGlobStar, cb)
else
  this._processReaddir(prefix, read, abs, remain, index, inGlobStar, cb)
}

Glob.prototype._processReaddir = function (prefix, read, abs, remain, index, inGlobStar, cb) {
var self = this
this._readdir(abs, inGlobStar, function (er, entries) {
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._processReaddir"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_processReaddir (prefix, read, abs, remain, index, inGlobStar)](#apidoc.element.glob.GlobSync.prototype._processReaddir)
- description and source-code
```javascript
_processReaddir = function (prefix, read, abs, remain, index, inGlobStar) {
  var entries = this._readdir(abs, inGlobStar)

  // if the abs isn't a dir, then nothing can match!
  if (!entries)
    return

  // It will only match dot entries if it starts with a dot, or if
  // dot is set.  Stuff like @(.foo|.bar) isn't allowed.
  var pn = remain[0]
  var negate = !!this.minimatch.negate
  var rawGlob = pn._glob
  var dotOk = this.dot || rawGlob.charAt(0) === '.'

  var matchedEntries = []
  for (var i = 0; i < entries.length; i++) {
    var e = entries[i]
    if (e.charAt(0) !== '.' || dotOk) {
      var m
      if (negate && !prefix) {
        m = !e.match(pn)
      } else {
        m = e.match(pn)
      }
      if (m)
        matchedEntries.push(e)
    }
  }

  var len = matchedEntries.length
  // If there are no matched entries, then nothing matches.
  if (len === 0)
    return

  // if this is the last remaining pattern bit, then no need for
  // an additional stat *unless* the user has specified mark or
  // stat explicitly.  We know they exist, since readdir returned
  // them.

  if (remain.length === 1 && !this.mark && !this.stat) {
    if (!this.matches[index])
      this.matches[index] = Object.create(null)

    for (var i = 0; i < len; i ++) {
      var e = matchedEntries[i]
      if (prefix) {
        if (prefix.slice(-1) !== '/')
          e = prefix + '/' + e
        else
          e = prefix + e
      }

      if (e.charAt(0) === '/' && !this.nomount) {
        e = path.join(this.root, e)
      }
      this._emitMatch(index, e)
    }
    // This was the last one, and no stats were needed
    return
  }

  // now test all matched entries as stand-ins for that part
  // of the pattern.
  remain.shift()
  for (var i = 0; i < len; i ++) {
    var e = matchedEntries[i]
    var newPattern
    if (prefix)
      newPattern = [prefix, e]
    else
      newPattern = [e]
    this._process(newPattern.concat(remain), index, inGlobStar)
  }
}
```
- example usage
```shell
...
if (childrenIgnored(this, read))
  return cb()

var isGlobStar = remain[0] === minimatch.GLOBSTAR
if (isGlobStar)
  this._processGlobStar(prefix, read, abs, remain, index, inGlobStar, cb)
else
  this._processReaddir(prefix, read, abs, remain, index, inGlobStar, cb)
}

Glob.prototype._processReaddir = function (prefix, read, abs, remain, index, inGlobStar, cb) {
var self = this
this._readdir(abs, inGlobStar, function (er, entries) {
  return self._processReaddir2(prefix, read, abs, remain, index, inGlobStar, entries, cb)
})
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._processSimple"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_processSimple (prefix, index)](#apidoc.element.glob.GlobSync.prototype._processSimple)
- description and source-code
```javascript
_processSimple = function (prefix, index) {
  // XXX review this.  Shouldn't it be doing the mounting etc
  // before doing stat?  kinda weird?
  var exists = this._stat(prefix)

  if (!this.matches[index])
    this.matches[index] = Object.create(null)

  // If it doesn't exist, then just mark the lack of results
  if (!exists)
    return

  if (prefix && isAbsolute(prefix) && !this.nomount) {
    var trail = /[\/\\]$/.test(prefix)
    if (prefix.charAt(0) === '/') {
      prefix = path.join(this.root, prefix)
    } else {
      prefix = path.resolve(this.root, prefix)
      if (trail)
        prefix += '/'
    }
  }

  if (process.platform === 'win32')
    prefix = prefix.replace(/\\/g, '/')

  // Mark this as a match
  this._emitMatch(index, prefix)
}
```
- example usage
```shell
...
  // now n is the index of the first one that is *not* a string.

  // see if there's anything else
  var prefix
  switch (n) {
// if not, then this is rather simple
case pattern.length:
  this._processSimple(pattern.join('/'), index, cb)
  return

case 0:
  // pattern *starts* with some non-trivial item.
  // going to readdir(cwd), but not include the prefix in matches.
  prefix = null
  break
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._readdir"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_readdir (abs, inGlobStar)](#apidoc.element.glob.GlobSync.prototype._readdir)
- description and source-code
```javascript
_readdir = function (abs, inGlobStar) {
  var entries

  if (inGlobStar && !ownProp(this.symlinks, abs))
    return this._readdirInGlobStar(abs)

  if (ownProp(this.cache, abs)) {
    var c = this.cache[abs]
    if (!c || c === 'FILE')
      return null

    if (Array.isArray(c))
      return c
  }

  try {
    return this._readdirEntries(abs, fs.readdirSync(abs))
  } catch (er) {
    this._readdirError(abs, er)
    return null
  }
}
```
- example usage
```shell
...
  this._processGlobStar(prefix, read, abs, remain, index, inGlobStar, cb)
else
  this._processReaddir(prefix, read, abs, remain, index, inGlobStar, cb)
}

Glob.prototype._processReaddir = function (prefix, read, abs, remain, index, inGlobStar, cb) {
var self = this
this._readdir(abs, inGlobStar, function (er, entries) {
  return self._processReaddir2(prefix, read, abs, remain, index, inGlobStar, entries, cb)
})
}

Glob.prototype._processReaddir2 = function (prefix, read, abs, remain, index, inGlobStar, entries, cb) {

// if the abs isn't a dir, then nothing can match!
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._readdirEntries"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_readdirEntries (abs, entries)](#apidoc.element.glob.GlobSync.prototype._readdirEntries)
- description and source-code
```javascript
_readdirEntries = function (abs, entries) {
  // if we haven't asked to stat everything, then just
  // assume that everything in there exists, so we can avoid
  // having to stat it a second time.
  if (!this.mark && !this.stat) {
    for (var i = 0; i < entries.length; i ++) {
      var e = entries[i]
      if (abs === '/')
        e = abs + e
      else
        e = abs + '/' + e
      this.cache[e] = true
    }
  }

  this.cache[abs] = entries

  // mark and cache dir-ness
  return entries
}
```
- example usage
```shell
...
}

function readdirCb (self, abs, cb) {
return function (er, entries) {
  if (er)
    self._readdirError(abs, er, cb)
  else
    self._readdirEntries(abs, entries, cb)
}
}

Glob.prototype._readdirEntries = function (abs, entries, cb) {
if (this.aborted)
  return
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._readdirError"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_readdirError (f, er)](#apidoc.element.glob.GlobSync.prototype._readdirError)
- description and source-code
```javascript
_readdirError = function (f, er) {
  // handle errors, and cache the information
  switch (er.code) {
    case 'ENOTSUP': // https://github.com/isaacs/node-glob/issues/205
    case 'ENOTDIR': // totally normal. means it *does* exist.
      var abs = this._makeAbs(f)
      this.cache[abs] = 'FILE'
      if (abs === this.cwdAbs) {
        var error = new Error(er.code + ' invalid cwd ' + this.cwd)
        error.path = this.cwd
        error.code = er.code
        throw error
      }
      break

    case 'ENOENT': // not terribly unusual
    case 'ELOOP':
    case 'ENAMETOOLONG':
    case 'UNKNOWN':
      this.cache[this._makeAbs(f)] = false
      break

    default: // some unusual error.  Treat as failure.
      this.cache[this._makeAbs(f)] = false
      if (this.strict)
        throw er
      if (!this.silent)
        console.error('glob error', er)
      break
  }
}
```
- example usage
```shell
...
var self = this
fs.readdir(abs, readdirCb(this, abs, cb))
}

function readdirCb (self, abs, cb) {
return function (er, entries) {
  if (er)
    self._readdirError(abs, er, cb)
  else
    self._readdirEntries(abs, entries, cb)
}
}

Glob.prototype._readdirEntries = function (abs, entries, cb) {
if (this.aborted)
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._readdirInGlobStar"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_readdirInGlobStar (abs)](#apidoc.element.glob.GlobSync.prototype._readdirInGlobStar)
- description and source-code
```javascript
_readdirInGlobStar = function (abs) {
  // follow all symlinked directories forever
  // just proceed as if this is a non-globstar situation
  if (this.follow)
    return this._readdir(abs, false)

  var entries
  var lstat
  var stat
  try {
    lstat = fs.lstatSync(abs)
  } catch (er) {
    if (er.code === 'ENOENT') {
      // lstat failed, doesn't exist
      return null
    }
  }

  var isSym = lstat && lstat.isSymbolicLink()
  this.symlinks[abs] = isSym

  // If it's not a symlink or a dir, then it's definitely a regular file.
  // don't bother doing a readdir in that case.
  if (!isSym && lstat && !lstat.isDirectory())
    this.cache[abs] = 'FILE'
  else
    entries = this._readdir(abs, false)

  return entries
}
```
- example usage
```shell
...

  cb = inflight('readdir\0'+abs+'\0'+inGlobStar, cb)
  if (!cb)
return

  //console.error('RD %j %j', +inGlobStar, abs)
  if (inGlobStar && !ownProp(this.symlinks, abs))
return this._readdirInGlobStar(abs, cb)

  if (ownProp(this.cache, abs)) {
var c = this.cache[abs]
if (!c || c === 'FILE')
  return cb()

if (Array.isArray(c))
...
```

#### <a name="apidoc.element.glob.GlobSync.prototype._stat"></a>[function <span class="apidocSignatureSpan">glob.GlobSync.prototype.</span>_stat (f)](#apidoc.element.glob.GlobSync.prototype._stat)
- description and source-code
```javascript
_stat = function (f) {
  var abs = this._makeAbs(f)
  var needDir = f.slice(-1) === '/'

  if (f.length > this.maxLength)
    return false

  if (!this.stat && ownProp(this.cache, abs)) {
    var c = this.cache[abs]

    if (Array.isArray(c))
      c = 'DIR'

    // It exists, but maybe not how we need it
    if (!needDir || c === 'DIR')
      return c

    if (needDir && c === 'FILE')
      return false

    // otherwise we have to stat, because maybe c=true
    // if we know it exists, but not what it is.
  }

  var exists
  var stat = this.statCache[abs]
  if (!stat) {
    var lstat
    try {
      lstat = fs.lstatSync(abs)
    } catch (er) {
      if (er && (er.code === 'ENOENT' || er.code === 'ENOTDIR')) {
        this.statCache[abs] = false
        return false
      }
    }

    if (lstat && lstat.isSymbolicLink()) {
      try {
        stat = fs.statSync(abs)
      } catch (er) {
        stat = lstat
      }
    } else {
      stat = lstat
    }
  }

  this.statCache[abs] = stat

  var c = true
  if (stat)
    c = stat.isDirectory() ? 'DIR' : 'FILE'

  this.cache[abs] = this.cache[abs] || c

  if (needDir && c === 'FILE')
    return false

  return c
}
```
- example usage
```shell
...
cb()
}

Glob.prototype._processSimple = function (prefix, index, cb) {
// XXX review this.  Shouldn't it be doing the mounting etc
// before doing stat?  kinda weird?
var self = this
this._stat(prefix, function (er, exists) {
  self._processSimple2(prefix, index, er, exists, cb)
})
}
Glob.prototype._processSimple2 = function (prefix, index, er, exists, cb) {

//console.error('ps2', prefix, exists)
...
```



# <a name="apidoc.module.glob.sync"></a>[module glob.sync](#apidoc.module.glob.sync)

#### <a name="apidoc.element.glob.sync.sync"></a>[function <span class="apidocSignatureSpan">glob.</span>sync (pattern, options)](#apidoc.element.glob.sync.sync)
- description and source-code
```javascript
function globSync(pattern, options) {
  if (typeof options === 'function' || arguments.length === 3)
    throw new TypeError('callback provided to sync glob\n'+
                        'See: https://github.com/isaacs/node-glob/issues/167')

  return new GlobSync(pattern, options).found
}
```
- example usage
```shell
...
* 'options' '{Object}'
* 'cb' '{Function}'
  * 'err' '{Error | null}'
  * 'matches' '{Array<String>}' filenames found matching the pattern

Perform an asynchronous glob search.

## glob.sync(pattern, [options])

* 'pattern' '{String}' Pattern to be matched
* 'options' '{Object}'
* return: '{Array<String>}' filenames found matching the pattern

Perform a synchronous glob search.
...
```

#### <a name="apidoc.element.glob.sync.GlobSync"></a>[function <span class="apidocSignatureSpan">glob.sync.</span>GlobSync (pattern, options)](#apidoc.element.glob.sync.GlobSync)
- description and source-code
```javascript
function GlobSync(pattern, options) {
  if (!pattern)
    throw new Error('must provide pattern')

  if (typeof options === 'function' || arguments.length === 3)
    throw new TypeError('callback provided to sync glob\n'+
                        'See: https://github.com/isaacs/node-glob/issues/167')

  if (!(this instanceof GlobSync))
    return new GlobSync(pattern, options)

  setopts(this, pattern, options)

  if (this.noprocess)
    return this

  var n = this.minimatch.set.length
  this.matches = new Array(n)
  for (var i = 0; i < n; i ++) {
    this._process(this.minimatch.set[i], i, false)
  }
  this._finish()
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
