[![Build Status][travis_badge]][travis_link] [![js-standard-style][js_standard_badge]][js_standard_link]



# openapi-mock

- *alpha version* of a library providing mock data for Open API 3.0 specifications. Created due to [swagger-parser](https://github.com/BigstickCarpet/swagger-parser) dragging behind, and entire node-swagger ecosystem put on-hold, with no forseeable replacement. This is way simpler implementation, but enables specific use-case.

## Example

```javascript
const Mock = require('openapi-mock')

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



[js_standard_badge]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square
[js_standard_link]:  https://github.com/feross/standard
[travis_badge]: https://travis-ci.org/unjello/openapi-mock.svg?branch=master
[travis_link]:  https://travis-ci.org/unjello/openapi-mock
