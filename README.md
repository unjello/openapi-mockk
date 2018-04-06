[![npm version][npm_badge]][npm_link] [![Build Status][travis_badge]][travis_link] [![downloads][npm_dl_badge]][npm_dl_link] [![js-standard-style][js_standard_badge]][js_standard_link]

# openapi-mockk

- *alpha version* of a library providing mock data for Open API 3.0 specifications. Created due to [swagger-parser](https://github.com/BigstickCarpet/swagger-parser) dragging behind, and entire node-swagger ecosystem put on-hold, with no forseeable replacement. This is way simpler implementation, but enables specific use-case.

## Example

```javascript
const Mock = require('openapi-mockk')

Mock(args.api).responses({
  path,
  operation,
  response: '200',
  content,
}).then(mock => {
  console.log(mock[path][operation].responses)
})
```

## License

- Unlicense (~Public Domain)

## Related Work

- https://github.com/subeeshcbabu/swagmock/ - way more advanced mock, but for swagger 2.0 schema
- https://github.com/BigstickCarpet/swagger-parser - swagger 2.0 parser


[npm_badge]: https://img.shields.io/npm/v/openapi-mockk.svg?style=flat-square
[npm_link]:  https://npmjs.org/package/openapi-mockk
[js_standard_badge]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square
[js_standard_link]:  https://github.com/feross/standard
[travis_badge]: https://travis-ci.org/unjello/openapi-mockk.svg?branch=master
[travis_link]:  https://travis-ci.org/unjello/openapi-mockk
[npm_dl_badge]: http://img.shields.io/npm/dm/openapi-mockk.svg?style=flat-square
[npm_dl_link]: https://npmjs.org/package/openapi-mockk