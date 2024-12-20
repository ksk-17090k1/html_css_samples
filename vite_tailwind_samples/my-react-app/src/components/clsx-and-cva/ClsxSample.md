# clsxの使い方

refs:[GitHub - lukeed/clsx: A tiny (239B) utility for constructing `className` strings conditionally.](https://github.com/lukeed/clsx)

```tsx
import clsx from "clsx";
// or
import { clsx } from "clsx";

// Strings (variadic)
clsx("foo", true && "bar", "baz");
//=> 'foo bar baz'

// Objects
clsx({ foo: true, bar: false, baz: isTrue() });
//=> 'foo baz'

// Objects (variadic)
clsx({ foo: true }, { bar: false }, null, { "--foobar": "hello" });
//=> 'foo --foobar'

// Arrays
clsx(["foo", 0, false, "bar"]);
//=> 'foo bar'

// Arrays (variadic)
clsx(["foo"], ["", 0, false, "bar"], [["baz", [["hello"], "there"]]]);
//=> 'foo bar baz hello there'

// Kitchen sink (with nesting)
clsx(
  "foo",
  [1 && "bar", { baz: false, bat: null }, ["hello", ["world"]]],
  "cya",
);
//=> 'foo bar hello world cya'
```
