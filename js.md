```js
const games = ['foo', 'bar', 'baz']
const [game] = games
console.log(game)
// 'foo'
```

```js
Array.from([1, 2, 3], x => x * 2)
// [2, 4, 6]

Array.from({length: 5}, (v, i) => i)
// [0, 1, 2, 3, 4]
```

```js
function foo (param1, param2) {
  // param1 and param2 are parameters
}

foo(8, 7)
// 8 and 7 are arguments
```

```js
(async function a () {
  const r = await Promise.race([
    new Promise((resolve, reject) => {
      setTimeout(resolve, 2000, 'foo')
    }),
    new Promise((resolve, reject) => {
      setTimeout(resolve, 1000, 'bar')
    })
  ])
  console.log(r)
})()

// bar
```
---

Node.js
```js
const util = require('util')
const obj = {
  it: 'will',
  print: {
    out: {
      the: ['full', 'object']
    }
  }
}
console.log(util.inspect(obj, { showHidden: false, depth: null }))

// { it: 'will', print: { out: { the: [ 'full', 'object' ] } } }
```
