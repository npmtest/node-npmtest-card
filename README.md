# npmtest-card

#### test coverage for  [card (v2.2.1)](https://github.com/jessepollak/card#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-card.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-card) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-card.svg)](https://travis-ci.org/npmtest/node-npmtest-card)

#### Card lets you add an interactive, CSS3 credit card animation to your credit card form to help your users through the process.

[![NPM](https://nodei.co/npm/card.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/card)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-card/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-card/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-card/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-card/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-card/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-card/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-card/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-card/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-card/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-card/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-card/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-card/build/test-report.html](https://npmtest.github.io/node-npmtest-card/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-card/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-card/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-card/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-card/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-card/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-card/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-card/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-card/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jesse Pollak"
    },
    "bugs": {
        "url": "https://github.com/jessepollak/card/issues"
    },
    "contributors": [
        {
            "name": "Jesse Pollak"
        },
        {
            "name": "Daniel Juhl"
        }
    ],
    "dependencies": {
        "node.extend": "~1.1.3",
        "payment": "^2.2.1",
        "qj": "^2.0.0"
    },
    "description": "Card lets you add an interactive, CSS3 credit card animation to your credit card form to help your users through the process.",
    "devDependencies": {
        "bower": "~1.7.9",
        "coffee-loader": "^0.7.2",
        "coffee-script": "~1.10.0",
        "css-loader": "^0.23.1",
        "event-stream": "^3.3.1",
        "glob": "^7.0.5",
        "jquery": "~3.0.0",
        "node-sass": "^3.8.0",
        "nodemon": "~1.9.2",
        "replace": "^0.3.0",
        "rimraf": "^2.5.4",
        "run-sequence": "~1.2.1",
        "sass-loader": "^3.2.2",
        "style-loader": "^0.13.1",
        "underscore": "^1.8.3",
        "vinyl-source-stream": "^1.1.0",
        "webpack": "^1.13.1",
        "webpack-dev-server": "^1.14.1"
    },
    "directories": {},
    "dist": {
        "shasum": "ec5f058d07bc89b98fb815560e0e70749785bfbb",
        "tarball": "https://registry.npmjs.org/card/-/card-2.2.1.tgz"
    },
    "gitHead": "d6d2845c16a6f450ecda87f7c3c51155eec9b303",
    "homepage": "https://github.com/jessepollak/card#readme",
    "main": "lib/card.js",
    "maintainers": [
        {
            "name": "jessepollak"
        }
    ],
    "name": "card",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/jessepollak/card.git"
    },
    "scripts": {
        "clean": "rimraf ./lib/ && rimraf ./dist/",
        "compile": "npm run clean && npm run compile:lib && npm run compile:dist",
        "compile:dist": "npm run env NODE_ENV=production && webpack",
        "compile:lib": "coffee --compile -o ./lib/ ./src/coffee/card.coffee && node-sass ./src/scss/card.scss -o lib/ && replace '../scss/card.scss' './card.css' lib/card.js",
        "development": "webpack-dev-server --hot --inline",
        "postpublish": "git push origin master && git push --tags",
        "prepublish": "npm run env NODE_ENV=production && npm run compile",
        "preversion": "npm run compile",
        "test": "karma start --single-run --browsers PhantomJS"
    },
    "version": "2.2.1"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
