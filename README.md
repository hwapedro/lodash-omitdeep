# lodash-omit-deep
> Lodash omitDeep/omitDeepBy object key/value recursively

lodash-omit-deep allows you to execute lodash omit, omitBy functions recursively.
## Install

Install with [npm](https://www.npmjs.com/)

```sh
$ npm i lodash-omit-deep- --save
```
Install with [yarn](https://yarnpkg.com/)

```sh
$ yarn add lodash-omit-deep
```
## Usage
### omitDeep
```js
import { omitDeep } from 'lodash-omit-deep';
omitDeep({a: "a", b: "b", c: {b: "b", d: {b: "b", f: "f"}}}, "b");
//=> {a: "a", c: {d: {f: "f"}}}
omitDeep({a: "a", b: "b", c: {b: "b", d: {b: "b", f: "f"}}}, ["a", "b"]);
//=> {c: {d: {f: "f"}}}
```
### omitByDeep
```js
import { omitDeepBy } from 'lodash-omit-deep';
import isNil from 'lodash/isNil';
import isNumber from 'lodash/isNumber';

omitDeep({a: "a", b: null, c: {b: "b", d: {b: "b", f: null}}}, isNil);
//=> {a: "a", c: {b: "b", d: {b: "b"}}}
omitDeep({a: 2, b: "b", c: {b: 4, d: {b: 1, f: "f"}}}, isNumber);
//=> {b: "b", c: {d: {f: "f"}}}
```

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/hwapedro/lodash-omit-deep/issues/new)

## Author

+ [github/hwapedro](https://github.com/hwapedro)


## License

Released under the MIT license.
