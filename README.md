# api documentation for  swagger-client (v3.0.3)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-swagger-client.svg)](https://travis-ci.org/npmdoc/node-npmdoc-swagger-client)
#### SwaggerJS - a collection of interfaces for OAI specs

[![NPM](https://nodei.co/npm/swagger-client.png?downloads=true)](https://www.npmjs.com/package/swagger-client)

[![apidoc](https://npmdoc.github.io/node-npmdoc-swagger-client/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-swagger_client_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-swagger-client/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-swagger-client/build/screen-capture.npmPackageListing.svg)



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
            "name": "Anna Bodnia",
            "email": "anna.bodnia@gmail.com"
        },
        {
            "name": "Buu Nguyen",
            "email": "buunguyen@gmail.com"
        },
        {
            "name": "Josh Ponelat",
            "email": "jponelat@gmail.com"
        },
        {
            "name": "Kyle Shockey",
            "email": "kyleshockey1@gmail.com"
        },
        {
            "name": "Sahar Jafari",
            "email": "shr.jafari@gmail.com"
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
        "node-inspector": "0.12.8",
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
        "shasum": "ff1362510be5a8978864a91ad6af5bae1fa2a6aa",
        "tarball": "https://registry.npmjs.org/swagger-client/-/swagger-client-3.0.3.tgz"
    },
    "gitHead": "bcb69e25b5a90a77239dc37cbae5fbdcdee0c06f",
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
            "name": "swagger-api",
            "email": "apiteam@swagger.io"
        }
    ],
    "name": "swagger-client",
    "optionalDependencies": {
        "node-inspector": "0.12.8"
    },
    "readme": "ERROR: No README data found!",
    "scripts": {
        "build": "NODE_ENV=production webpack -p --config ./webpack.config.js && NODE_ENV=production webpack -p --config ./webpack.bundle.config.js ",
        "deps-check": "npm run deps-license && npm run deps-size",
        "deps-license": "license-checker --production --csv --out $npm_package_config_deps_check_dir/licenses.csv && license-checker --development --csv --out $npm_package_config_deps_check_dir/licenses-dev.csv",
        "deps-size": "webpack -p --config webpack.check.js --json | webpack-bundle-size-analyzer >| $npm_package_config_deps_check_dir/sizes.txt",
        "inspector": "node-debug",
        "lint": "eslint src/ test/",
        "test": "NODE_ENV=test node --debug ./node_modules/.bin/_mocha --recursive --compilers js:babel-core/register",
        "test:watch": "npm run test -- -w",
        "watch": "webpack --config webpack.config.js --watch --progress"
    },
    "version": "3.0.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module swagger-client](#apidoc.module.swagger-client)
1.  [function <span class="apidocSignatureSpan">swagger-client.</span>buildRequest (e)](#apidoc.element.swagger-client.buildRequest)
1.  [function <span class="apidocSignatureSpan">swagger-client.</span>clearCache ()](#apidoc.element.swagger-client.clearCache)
1.  [function <span class="apidocSignatureSpan">swagger-client.</span>execute (e)](#apidoc.element.swagger-client.execute)
1.  [function <span class="apidocSignatureSpan">swagger-client.</span>http (e)](#apidoc.element.swagger-client.http)
1.  [function <span class="apidocSignatureSpan">swagger-client.</span>makeApisTagOperation ()](#apidoc.element.swagger-client.makeApisTagOperation)
1.  [function <span class="apidocSignatureSpan">swagger-client.</span>makeHttp ()](#apidoc.element.swagger-client.makeHttp)
1.  [function <span class="apidocSignatureSpan">swagger-client.</span>resolve (e)](#apidoc.element.swagger-client.resolve)
1.  [function <span class="apidocSignatureSpan">swagger-client.</span>serializeHeaders ()](#apidoc.element.swagger-client.serializeHeaders)
1.  [function <span class="apidocSignatureSpan">swagger-client.</span>serializeRes (e, t, r)](#apidoc.element.swagger-client.serializeRes)
1.  object <span class="apidocSignatureSpan">swagger-client.</span>parameterBuilders

#### [module swagger-client.parameterBuilders](#apidoc.module.swagger-client.parameterBuilders)
1.  [function <span class="apidocSignatureSpan">swagger-client.parameterBuilders.</span>body (e)](#apidoc.element.swagger-client.parameterBuilders.body)
1.  [function <span class="apidocSignatureSpan">swagger-client.parameterBuilders.</span>formData (e)](#apidoc.element.swagger-client.parameterBuilders.formData)
1.  [function <span class="apidocSignatureSpan">swagger-client.parameterBuilders.</span>header (e)](#apidoc.element.swagger-client.parameterBuilders.header)
1.  [function <span class="apidocSignatureSpan">swagger-client.parameterBuilders.</span>path (e)](#apidoc.element.swagger-client.parameterBuilders.path)
1.  [function <span class="apidocSignatureSpan">swagger-client.parameterBuilders.</span>query (e)](#apidoc.element.swagger-client.parameterBuilders.query)



# <a name="apidoc.module.swagger-client"></a>[module swagger-client](#apidoc.module.swagger-client)

#### <a name="apidoc.element.swagger-client.buildRequest"></a>[function <span class="apidocSignatureSpan">swagger-client.</span>buildRequest (e)](#apidoc.element.swagger-client.buildRequest)
- description and source-code
```javascript
function u(e){var t=e.spec,r=e.operationId,n=e.parameters,a=e.securities,u=e.requestContentType,i=e.responseContentType,o=e.parameterBuilders
,s=e.scheme,c=e.requestInterceptor,l=e.responseInterceptor,d=e.contextUrl;o=o||C;var h={url:f({spec:t,scheme:s,contextUrl:d}),headers
:{}};if(c&&(h.requestInterceptor=c),l&&(h.responseInterceptor=l),!r)return h;var v=(0,E.getOperationRaw)(t,r),m=v.operation,g=void
 0===m?{}:m,y=v.method,b=v.pathName;return h.url+=b,h.method=(""+y).toUpperCase(),n=n||{},i&&(h.headers.accept=i),u&&(h.headers["
content-type"]=u),M(g.parameters).concat(M(t.paths[b].parameters)).forEach(function(e){var r=o[e.in],a=void 0;if("body"===e.in&&
e.schema&&e.schema.properties&&(a=n),a=e&&e.name&&n[e.name],void 0!==e.default&&void 0===a&&(a=e.default),void 0===a&&e.required
&&!e.allowEmptyValue)throw new Error("Required parameter "+e.name+" is not provided");r&&r({req:h,parameter:e,value:a,operation:
g,spec:t})}),h=p({request:h,securities:a,operation:g,spec:t}),(0,A.mergeInQueryOrForm)(h),h}
```
- example usage
```shell
...
  securities,
  requestContentType,
  responseContentType
}

// Creates a request object compatible with HTTP client interface.
// If 'pathName' and 'method', then those are used instead of operationId.
const req = Swagger.buildRequest(...params)
Swagger.execute({http, ...params})
'''

Tags Interface
--------------
A JS client for operations. We're currently using the 'apis[tag][operationId]:ExecuteFunction' interface, which can be disabled
entirely using 'Swagger({disableInterfaces: true})' if you don't need it.
...
```

#### <a name="apidoc.element.swagger-client.clearCache"></a>[function <span class="apidocSignatureSpan">swagger-client.</span>clearCache ()](#apidoc.element.swagger-client.clearCache)
- description and source-code
```javascript
function u(){c.plugins.refs.clearCache()}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-client.execute"></a>[function <span class="apidocSignatureSpan">swagger-client.</span>execute (e)](#apidoc.element.swagger-client.execute)
- description and source-code
```javascript
function a(e){var t=e.http,r=e.fetch,n=e.spec,a=e.operationId,u=e.pathName,i=e.method,o=e.parameters,s=e.securities,c=(0,y.default
)(e,["http","fetch","spec","operationId","pathName","method","parameters","securities"]);return t=t||r||_.default,u&&i&&(a=(0,E.
idFromPathMethod)(u,i)),t(j.buildRequest((0,m.default)({spec:n,operationId:a,parameters:o,securities:s},c)))}
```
- example usage
```shell
...
  requestContentType,
  responseContentType
}

// Creates a request object compatible with HTTP client interface.
// If 'pathName' and 'method', then those are used instead of operationId.
const req = Swagger.buildRequest(...params)
Swagger.execute({http, ...params})
'''

Tags Interface
--------------
A JS client for operations. We're currently using the 'apis[tag][operationId]:ExecuteFunction' interface, which can be disabled
entirely using 'Swagger({disableInterfaces: true})' if you don't need it.

OperationId's are meant to be unique within spec, if they're not we do the following:
...
```

#### <a name="apidoc.element.swagger-client.http"></a>[function <span class="apidocSignatureSpan">swagger-client.</span>http (e)](#apidoc.element.swagger-client.http)
- description and source-code
```javascript
function a(e){var t=arguments.length>1&&void 0!==arguments[1]?arguments[1]:{};"object"===(void 0===e?"undefined":(0,y.default)(e
))&&(t=e,e=t.url),t.headers=t.headers||{},A.mergeInQueryOrForm(t),t.requestInterceptor&&(t=t.requestInterceptor(t)||t);var r=t.headers
["content-type"]||t.headers["Content-Type"];return/multipart\/form-data/i.test(r)&&(delete t.headers["content-type"],delete t.headers["Content-Type"]),(0,x.default)(t.url,t).then(function(r){return A.serializeRes(r,e,t).then(function(e){return t.responseInterceptor&&(e=t.responseInterceptor(e)||e),e})})}
```
- example usage
```shell
...
1. TryItOut Executor
1. Tags Interface
1. JS API

HTTP Client
-----------

'Swagger.http(req)' exposes a [Fetch-like interface](https://github.com/matthew-andrews/isomorphic-fetch) with a tweak: allowing
 'url' in the request object so that it can be passed around and mutated. It extends Fetch to support request and response interceptor
 and perform response & headers serialization. This method could be overridden to change how SwaggerJS performs HTTP requests.

'''js
// Fetch-like, but support 'url'
const request = {
url,
query,
method,
...
```

#### <a name="apidoc.element.swagger-client.makeApisTagOperation"></a>[function <span class="apidocSignatureSpan">swagger-client.</span>makeApisTagOperation ()](#apidoc.element.swagger-client.makeApisTagOperation)
- description and source-code
```javascript
function i(){var e=arguments.length>0&&void 0!==arguments[0]?arguments[0]:{},t=v.makeExecute(e);return{apis:v.mapTagOperations({
spec:e.spec,cb:t})}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-client.makeHttp"></a>[function <span class="apidocSignatureSpan">swagger-client.</span>makeHttp ()](#apidoc.element.swagger-client.makeHttp)
- description and source-code
```javascript
makeHttp = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-client.resolve"></a>[function <span class="apidocSignatureSpan">swagger-client.</span>resolve (e)](#apidoc.element.swagger-client.resolve)
- description and source-code
```javascript
function i(e){var t=e.http,r=e.fetch,n=e.spec,u=e.url,i=e.mode,o=e.allowMetaPatches,p=void 0===o||o;t=r||t||s.default,n?c.plugins
.refs.docCache[u]=n:n={$ref:u},c.plugins.refs.fetchJSON=a(t);var d=[c.plugins.refs];return"strict"!==i&&d.push(c.plugins.allOf),(
0,l.default)({spec:n,context:{baseDoc:u},plugins:d,allowMetaPatches:p}).then(f.normalizeSwagger)}
```
- example usage
```shell
...
})

'''

Swagger Spec Resolver
---------------------

'Swagger.resolve({url, spec, http})' resolves '$ref's (JSON-Refs) with the objects they point to.

'''js

Swagger.resolve({url, spec, http}).then((resolved) => {
  resolved.errors // resolution errors, if any
  resolved.spec   // the resolved spec
})
...
```

#### <a name="apidoc.element.swagger-client.serializeHeaders"></a>[function <span class="apidocSignatureSpan">swagger-client.</span>serializeHeaders ()](#apidoc.element.swagger-client.serializeHeaders)
- description and source-code
```javascript
function o(){var e=arguments.length>0&&void 0!==arguments[0]?arguments[0]:{},t={};return"function"==typeof e.forEach?(e.forEach(
function(e,r){void 0!==t[r]?(t[r]=Array.isArray(t[r])?t[r]:[t[r]],t[r].push(e)):t[r]=e}),t):t}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-client.serializeRes"></a>[function <span class="apidocSignatureSpan">swagger-client.</span>serializeRes (e, t, r)](#apidoc.element.swagger-client.serializeRes)
- description and source-code
```javascript
function i(e, t, r){var n=r.loadSpec,a=void 0!==n&&n,i={ok:e.ok,url:e.url||t,status:e.status,statusText:e.statusText,headers:o(e.headers
)},s=a||u(i.headers["content-type"]);return e[s?"text":"blob"]().then(function(e){if(i.text=e,i.data=e,s)try{var t=q.default.safeLoad
(e);i.body=t,i.obj=t}catch(e){i.parseError=e}return i})}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.swagger-client.parameterBuilders"></a>[module swagger-client.parameterBuilders](#apidoc.module.swagger-client.parameterBuilders)

#### <a name="apidoc.element.swagger-client.parameterBuilders.body"></a>[function <span class="apidocSignatureSpan">swagger-client.parameterBuilders.</span>body (e)](#apidoc.element.swagger-client.parameterBuilders.body)
- description and source-code
```javascript
function i(e){var t=e.req,r=e.value;t.body=r}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-client.parameterBuilders.formData"></a>[function <span class="apidocSignatureSpan">swagger-client.parameterBuilders.</span>formData (e)](#apidoc.element.swagger-client.parameterBuilders.formData)
- description and source-code
```javascript
function o(e){var t=e.req,r=e.value,n=e.parameter;t.form=t.form||{},(r||n.allowEmptyValue)&&(t.form[n.name]={value:r,allowEmptyValue
:n.allowEmptyValue,collectionFormat:n.collectionFormat})}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-client.parameterBuilders.header"></a>[function <span class="apidocSignatureSpan">swagger-client.parameterBuilders.</span>header (e)](#apidoc.element.swagger-client.parameterBuilders.header)
- description and source-code
```javascript
function s(e){var t=e.req,r=e.parameter,n=e.value;t.headers=t.headers||{},t.headers[r.name]=n}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-client.parameterBuilders.path"></a>[function <span class="apidocSignatureSpan">swagger-client.parameterBuilders.</span>path (e)](#apidoc.element.swagger-client.parameterBuilders.path)
- description and source-code
```javascript
function c(e){var t=e.req,r=e.value,n=e.parameter;t.url=t.url.replace("{"+n.name+"}",encodeURIComponent(r))}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-client.parameterBuilders.query"></a>[function <span class="apidocSignatureSpan">swagger-client.parameterBuilders.</span>query (e)](#apidoc.element.swagger-client.parameterBuilders.query)
- description and source-code
```javascript
function l(e){var t=e.req,r=e.value,n=e.parameter;if(t.query=t.query||{},r)t.query[n.name]={collectionFormat:n.collectionFormat,
value:r};else if(n.allowEmptyValue){var a=n.name;t.query[a]=t.query[a]||{},t.query[a].allowEmptyValue=!0}}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
