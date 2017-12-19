# `bury(obj, keypath, value)`

> Safely set a dot-notated path within a nested object, return undefined if the full key path does not exist, otherwise return the value set.

### Usage

`bury(object, keypath, value)`

```js
import bury from 'bury';

let obj = {
	a: {
		b: {
			c: 1
			d: undefined
			e: null
		}
	}
};

//use string dot notation for keys
bury(obj, 'a.b.c', 2) === 2;

//or use an array key
bury(obj, ['a', 'b', 'c'], 2) === 2;

//returns undefined if the full key path does not exist
bury(obj, 'a.b.c.f', "foo") === undefined;
```

### License

MIT

[tests]: https://github.com/kalmbach/bury/blob/master/test.js