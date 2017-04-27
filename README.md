# npmdoc-swagger-client

#### basic api documentation for  swagger-client (v3.0.7)  [![npm package](https://img.shields.io/npm/v/npmdoc-swagger-client.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-swagger-client) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-swagger-client.svg)](https://travis-ci.org/npmdoc/node-npmdoc-swagger-client)

#### SwaggerJS - a collection of interfaces for OAI specs

[![NPM](https://nodei.co/npm/swagger-client.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/swagger-client)

- [https://npmdoc.github.io/node-npmdoc-swagger-client/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-swagger-client/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-swagger-client/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-swagger-client/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-swagger-client/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-swagger-client/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "config": {
        "deps_check_dir": ".deps_check"
    },
    "contributors": [
        {
            "url": "in alphabetical order"
        },
        {
            "name": "Anna Bodnia"
        },
        {
            "name": "Buu Nguyen"
        },
        {
            "name": "Josh Ponelat"
        },
        {
            "name": "Kyle Shockey"
        },
        {
            "name": "Sahar Jafari"
        }
    ],
    "dependencies": {
        "babel-runtime": "^6.23.0",
        "btoa": "1.1.2",
        "deep-extend": "^0.4.1",
        "fast-json-patch": "^1.1.8",
        "isomorphic-fetch": "2.2.1",
        "isomorphic-form-data": "0.0.1",
        "js-yaml": "^3.8.1",
        "lodash": "4.16.2",
        "qs": "^6.3.0",
        "url": "^0.11.0"
    },
    "description": "SwaggerJS - a collection of interfaces for OAI specs",
    "devDependencies": {
        "babel-core": "^6.23.1",
        "babel-eslint": "^6.0.2",
        "babel-loader": "^6.3.2",
        "babel-plugin-transform-object-rest-spread": "6.16.0",
        "babel-plugin-transform-runtime": "6.15.0",
        "babel-preset-es2015": "^6.22.0",
        "clone": "^2.1.0",
        "deepmerge": "^1.3.0",
        "eslint": "^3.18.0",
        "eslint-config-airbnb-base": "^11.1.1",
        "eslint-plugin-import": "^2.2.0",
        "expect": "^1.20.2",
        "fetch-mock": "^5.9.3",
        "glob": "^7.1.1",
        "json-loader": "^0.5.4",
        "license-checker": "^8.0.3",
        "mocha": "^2.4.5",
        "traverse": "^0.6.6",
        "webpack": "^2.2.1",
        "webpack-bundle-size-analyzer": "^2.2.0",
        "xmock": "^0.3.0"
    },
    "directories": {},
    "dist": {
        "shasum": "5b30ea7a30db5dd8c4211a2b90338dce613dbaa3",
        "tarball": "https://registry.npmjs.org/swagger-client/-/swagger-client-3.0.7.tgz"
    },
    "gitHead": "503c1f4d6442c988b25355e18f5fce3824139864",
    "keywords": [
        "oai",
        "swagger",
        "js",
        "spec",
        "resolver",
        "json-refs"
    ],
    "license": "Apache-2.0",
    "main": "dist/index.js",
    "maintainers": [
        {
            "name": "swagger-api"
        }
    ],
    "name": "swagger-client",
    "optionalDependencies": {},
    "scripts": {
        "build": "NODE_ENV=production webpack -p --config ./webpack.config.js",
        "build-bundle": "NODE_ENV=production webpack -p --config ./webpack.bundle.config.js",
        "deps-check": "npm run deps-license && npm run deps-size",
        "deps-license": "license-checker --production --csv --out $npm_package_config_deps_check_dir/licenses.csv && license-checker --development --csv --out $npm_package_config_deps_check_dir/licenses-dev.csv",
        "deps-size": "webpack -p --config webpack.check.js --json | webpack-bundle-size-analyzer >| $npm_package_config_deps_check_dir/sizes.txt",
        "lint": "eslint src/ test/",
        "test": "NODE_ENV=test node --debug ./node_modules/.bin/_mocha --recursive --compilers js:babel-core/register",
        "test:watch": "npm run test -- -w",
        "watch": "webpack --config webpack.config.js --watch --progress"
    },
    "version": "3.0.7",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
