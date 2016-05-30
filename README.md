donot-cache-filesystem
======================

[![Build Status](https://travis-ci.org/donotjs/donot-cache-filesystem.svg?branch=master)](https://travis-ci.org/donotjs/donot-cache-filesystem)

File system cache engine for [donot](https://github.com/donotjs/donot).

# How to Use

Usage: `fsCache(cacheDir, options)`

## Example

		var http = require('http'),
		    donot = require('donot'),
		    fsCache = require('donot-cache-filesystem');

		var server = http.createServer(donot(__dirname + '/public', {
			cache: fsCache(yourCacheDir, {
				createDirectory: false
			})
		));

		server.listen(8000);

> Remark. It does not make sense to use caching without template engine plug-ins - as only template renderings are cached. See [donot](https://github.com/donotjs/donot) for available template plug-ins.

# Options

There is only one available option for this plug-in.

| Name                | Type    | Default | Description |
|:--------------------|:--------|:--------|:------------|
| **createDirectory** | Boolean | `false` | Create directory if it does not exist. |

# License

MIT
