# @sefr/nullable ✨

- [What does it do ?](#what-does-it-do--)
- [Compatibility](#compatibility-)
- [Dependencies](#dependencies-)
- [Installation](#installation-)
- [How to use](#how-to-use-)
- [Incorrect usages](#incorrect-usages-)
- [Credits](#credits-)
- [License](#license-)

## What does it do ? 💡

Provide a simple implementation of the `Nullable<T>` type which allow a value to be either `T` or `null`.

## Compatibility 🔧

| TypeScript | EcmaScript |
|------------|------------|
| \>= 2.8.0  | \>= ES2015 |

## Dependencies 🎱

This package is dependencies-free.

## Installation 💾

Nothing more than :

```shell
npm i -S @sefr/nullable
```

## How to use 📚

✅ Returning a success without content :

```typescript
import { Nullable } from "@sefr/nullable";

function doSomething(condition: boolean): Nullable<string> {
    if (condition) {
		return "toto";
    } else {
		return null;
    }
}

const toto: Nullable<string> = doSomething(true);
console.log(toto); // "toto"
const titi: Nullable<string> = doSomething(false);
console.log(titi); // null
```

## Incorrect usages ❌

❌ Returning `undefined` instead of `null` won't work at compilation time :

```typescript
import { Nullable } from "@sefr/nullable";

function doSomething(condition: boolean): Nullable<string> {
	if (condition) {
		return "toto";
	} else {
		return undefined;
	}
}
```

## Credits 📎

+ Developed with the awesome [TypeScript](https://www.typescriptlang.org/)

## License 📜

This software is available under the MIT License. See the [LICENSE](LICENSE.md) file for more informations.

⬆️ [Go back to top](#sefrnullable-)
