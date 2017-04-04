# api documentation for  [command-line-args (v4.0.2)](https://github.com/75lb/command-line-args#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-command-line-args.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-command-line-args) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-command-line-args.svg)](https://travis-ci.org/npmdoc/node-npmdoc-command-line-args)
#### A mature, feature-complete library to parse command-line options.

[![NPM](https://nodei.co/npm/command-line-args.png?downloads=true)](https://www.npmjs.com/package/command-line-args)

[![apidoc](https://npmdoc.github.io/node-npmdoc-command-line-args/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-command-line-args_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-command-line-args/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-command-line-args/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-command-line-args/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Lloyd Brookes",
        "email": "75pound@gmail.com"
    },
    "bin": {
        "command-line-args": "bin/cli.js"
    },
    "bugs": {
        "url": "https://github.com/75lb/command-line-args/issues"
    },
    "dependencies": {
        "array-back": "^1.0.4",
        "find-replace": "^1.0.3",
        "typical": "^2.6.0"
    },
    "description": "A mature, feature-complete library to parse command-line options.",
    "devDependencies": {
        "coveralls": "^2.11.15",
        "jsdoc-to-markdown": "^2.0.1",
        "test-runner": "^0.3.0"
    },
    "directories": {},
    "dist": {
        "shasum": "a99c2f28ceabcf26ac56d38e78b600ea3b57e650",
        "tarball": "https://registry.npmjs.org/command-line-args/-/command-line-args-4.0.2.tgz"
    },
    "gitHead": "3ccb02809c295d1fb31996c05dedfa85ebbdcc88",
    "homepage": "https://github.com/75lb/command-line-args#readme",
    "keywords": [
        "argv",
        "parse",
        "argument",
        "args",
        "option",
        "options",
        "parser",
        "parsing",
        "cli",
        "command",
        "line"
    ],
    "license": "MIT",
    "main": "lib/command-line-args.js",
    "maintainers": [
        {
            "name": "75lb",
            "email": "75pound@gmail.com"
        }
    ],
    "name": "command-line-args",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/75lb/command-line-args.git"
    },
    "scripts": {
        "cover": "istanbul cover ./node_modules/.bin/test-runner test/*.js && cat coverage/lcov.info | ./node_modules/.bin/coveralls && rm -rf coverage; echo",
        "docs": "jsdoc2md -l off -t jsdoc2md/README.hbs lib/*.js > README.md; echo",
        "test": "test-runner test/*.js"
    },
    "version": "4.0.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module command-line-args](#apidoc.module.command-line-args)
1.  object <span class="apidocSignatureSpan">command-line-args.</span>option

#### [module command-line-args.option](#apidoc.module.command-line-args.option)
1.  [function <span class="apidocSignatureSpan">command-line-args.option.</span>isOption (arg)](#apidoc.element.command-line-args.option.isOption)
1.  object <span class="apidocSignatureSpan">command-line-args.option.</span>combined
1.  object <span class="apidocSignatureSpan">command-line-args.option.</span>long
1.  object <span class="apidocSignatureSpan">command-line-args.option.</span>optEquals
1.  object <span class="apidocSignatureSpan">command-line-args.option.</span>short
1.  string <span class="apidocSignatureSpan">command-line-args.option.</span>VALUE_MARKER



# <a name="apidoc.module.command-line-args"></a>[module command-line-args](#apidoc.module.command-line-args)



# <a name="apidoc.module.command-line-args.option"></a>[module command-line-args.option](#apidoc.module.command-line-args.option)

#### <a name="apidoc.element.command-line-args.option.isOption"></a>[function <span class="apidocSignatureSpan">command-line-args.option.</span>isOption (arg)](#apidoc.element.command-line-args.option.isOption)
- description and source-code
```javascript
isOption(arg) { return this.short.test(arg) || this.long.test(arg) }
```
- example usage
```shell
...
   */
  validate (definitions, options) {
options = options || {}
let invalidOption

if (!options.partial) {
  const optionWithoutDefinition = this
    .filter(arg => option.isOption(arg))
    .some(arg => {
      if (definitions.get(arg) === undefined) {
        invalidOption = arg
        return true
      }
    })
  if (optionWithoutDefinition) {
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
