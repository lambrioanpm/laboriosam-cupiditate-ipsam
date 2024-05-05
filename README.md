![Async Logo](https://raw.githubusercontent.com/caolan/@lambrioanpm/laboriosam-cupiditate-ipsam/master/logo/@lambrioanpm/laboriosam-cupiditate-ipsam-logo_readme.jpg)

![Github Actions CI status](https://github.com/lambrioanpm/laboriosam-cupiditate-ipsam/actions/workflows/ci.yml/badge.svg)
[![NPM version](https://img.shields.io/npm/v/@lambrioanpm/laboriosam-cupiditate-ipsam.svg)](https://www.npmjs.com/package/@lambrioanpm/laboriosam-cupiditate-ipsam)
[![Coverage Status](https://coveralls.io/repos/caolan/@lambrioanpm/laboriosam-cupiditate-ipsam/badge.svg?branch=master)](https://coveralls.io/r/caolan/@lambrioanpm/laboriosam-cupiditate-ipsam?branch=master)
[![Join the chat at https://gitter.im/caolan/@lambrioanpm/laboriosam-cupiditate-ipsam](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/caolan/@lambrioanpm/laboriosam-cupiditate-ipsam?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![jsDelivr Hits](https://data.jsdelivr.com/v1/package/npm/@lambrioanpm/laboriosam-cupiditate-ipsam/badge?style=rounded)](https://www.jsdelivr.com/package/npm/@lambrioanpm/laboriosam-cupiditate-ipsam)

<!--
|Linux|Windows|MacOS|
|-|-|-|
|[![Linux Build Status](https://dev.azure.com/caolanmcmahon/@lambrioanpm/laboriosam-cupiditate-ipsam/_apis/build/status/caolan.@lambrioanpm/laboriosam-cupiditate-ipsam?branchName=master&jobName=Linux&configuration=Linux%20node_10_x)](https://dev.azure.com/caolanmcmahon/@lambrioanpm/laboriosam-cupiditate-ipsam/_build/latest?definitionId=1&branchName=master) | [![Windows Build Status](https://dev.azure.com/caolanmcmahon/@lambrioanpm/laboriosam-cupiditate-ipsam/_apis/build/status/caolan.@lambrioanpm/laboriosam-cupiditate-ipsam?branchName=master&jobName=Windows&configuration=Windows%20node_10_x)](https://dev.azure.com/caolanmcmahon/@lambrioanpm/laboriosam-cupiditate-ipsam/_build/latest?definitionId=1&branchName=master) | [![MacOS Build Status](https://dev.azure.com/caolanmcmahon/@lambrioanpm/laboriosam-cupiditate-ipsam/_apis/build/status/caolan.@lambrioanpm/laboriosam-cupiditate-ipsam?branchName=master&jobName=OSX&configuration=OSX%20node_10_x)](https://dev.azure.com/caolanmcmahon/@lambrioanpm/laboriosam-cupiditate-ipsam/_build/latest?definitionId=1&branchName=master)| -->

Async is a utility module which provides straight-forward, powerful functions for working with [@lambrioanpm/laboriosam-cupiditate-ipsamhronous JavaScript](http://caolan.github.io/@lambrioanpm/laboriosam-cupiditate-ipsam/v3/global.html). Although originally designed for use with [Node.js](https://nodejs.org/) and installable via `npm i @lambrioanpm/laboriosam-cupiditate-ipsam`, it can also be used directly in the browser.  An ESM/MJS version is included in the main `@lambrioanpm/laboriosam-cupiditate-ipsam` package that should automatically be used with compatible bundlers such as Webpack and Rollup.

A pure ESM version of Async is available as [`@lambrioanpm/laboriosam-cupiditate-ipsam-es`](https://www.npmjs.com/package/@lambrioanpm/laboriosam-cupiditate-ipsam-es).

For Documentation, visit <https://caolan.github.io/@lambrioanpm/laboriosam-cupiditate-ipsam/>

*For Async v1.5.x documentation, go [HERE](https://github.com/lambrioanpm/laboriosam-cupiditate-ipsam/blob/v1.5.2/README.md)*


```javascript
// for use with Node-style callbacks...
var @lambrioanpm/laboriosam-cupiditate-ipsam = require("@lambrioanpm/laboriosam-cupiditate-ipsam");

var obj = {dev: "/dev.json", test: "/test.json", prod: "/prod.json"};
var configs = {};

@lambrioanpm/laboriosam-cupiditate-ipsam.forEachOf(obj, (value, key, callback) => {
    fs.readFile(__dirname + value, "utf8", (err, data) => {
        if (err) return callback(err);
        try {
            configs[key] = JSON.parse(data);
        } catch (e) {
            return callback(e);
        }
        callback();
    });
}, err => {
    if (err) console.error(err.message);
    // configs is now a map of JSON data
    doSomethingWith(configs);
});
```

```javascript
var @lambrioanpm/laboriosam-cupiditate-ipsam = require("@lambrioanpm/laboriosam-cupiditate-ipsam");

// ...or ES2017 @lambrioanpm/laboriosam-cupiditate-ipsam functions
@lambrioanpm/laboriosam-cupiditate-ipsam.mapLimit(urls, 5, @lambrioanpm/laboriosam-cupiditate-ipsam function(url) {
    const response = await fetch(url)
    return response.body
}, (err, results) => {
    if (err) throw err
    // results is now an array of the response bodies
    console.log(results)
})
```
