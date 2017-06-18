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