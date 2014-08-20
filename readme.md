# CLI tools and node streams

The goal of this Markdown is to map CLI tools and node streaming modules.
Some of the CLI are well-known from UNIX, others are node modules as well.

Headlines are <CLI> - <node module>

## curl - request
`curl <url>`
```js
var request = require('request')
request('<url>')
```

## json-select - JSONStream
`json-select <query>`
```js
var select = require('JSONStream').parse
select('<query>')
```

## jsonmap - through2
`jsonmap "{a : this.b}"`
```js
var map = require('through2').obj
map(function (obj, enc, cb) {
  cb(this, {a: this.b})
})
```