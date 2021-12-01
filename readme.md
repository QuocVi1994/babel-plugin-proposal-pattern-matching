## Installation

With npm:
```sh
npm install --save-dev babel-plugin-proposal-pattern-matching
```

## Setup

### .babelrc

```json
{
  "plugins": ["babel-plugin-proposal-pattern-matching"]
}
```

#### Example

```js
import match from 'babel-plugin-proposal-pattern-matching/match'
const fib = n=>match(n)(
        (v=1)=>1,
        (v=2)=>1,
        _=>fib(_-1)+fib(_-2)
)

console.log(fib(10))
// -> 55
```

## LICENSE

MIT
