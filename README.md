# Random word generator

### A random word generator mainly being used for [FindSaaS](https://findsaas.vercel.app)

# Install Package 📦

Install the dependencies and devDependencies and start the server.

```sh
npm install arandomword
```

## Usage ✨

```js
import { generate } from "arandomword";


console.log(generate());
//output: 'wild'
```

## Donations ☕
[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/hellofaizan)

## Other Uses

```js
console.log(generate(5));
//output: ['wild', 'beautiful', 'became', 'wrapped', 'actually']

console.log(generate({ minLength: 5, maxLength: 5 }));
//output : 'world'

console.log(generate({ min: 3, max: 10 })); // the number of words in an array
//output: ['became', 'arrow', 'article', 'therefore']

console.log(generate({ exactly: 2 })); // just 2
//output: ['beside', 'between']

console.log(generate({ exactly: 5, join: " " }));
//output: 'army beautiful became if exactly'

console.log(generate({ exactly: 5, join: "" }));
//output: 'armybeautifulbecameifexactly'

console.log(generate({ exactly: 2, minLength: 4 })); // min length of each word also works with maxLength
//output: ['atom', 'window']

console.log(generate({ exactly: 2, minLength: 3, maxLength: 3 }));
//output: ['you, 'are']

console.log(generate({ exactly: 5, wordsPerString: 2 }));
//output: [ 'salt practical', 'also brief', 'country muscle', 'neighborhood beyond', 'grew pig' ]

console.log(generate({ exactly: 5, wordsPerString: 2, separator: "-" }));
//output: [ 'equator-variety', 'salt-usually', 'importance-becoming', 'stream-several', 'goes-fight' ]

console.log(
  generate({
    exactly: 5,
    wordsPerString: 2,
    formatter: (word) => word.toUpperCase(),
  })
);
//output: [ 'HAVING LOAD', 'LOST PINE', 'GAME SLOPE', 'SECRET GIANT', 'INDEED LOCATION' ]

console.log(
  generate({
    exactly: 5,
    wordsPerString: 2,
    formatter: (word, index) => {
      return index === 0
        ? word.slice(0, 1).toUpperCase().concat(word.slice(1))
        : word;
    },
  })
);
//output: [ 'Until smoke', 'Year strength', 'Pay knew', 'Fallen must', 'Chief arrow' ]

console.log(count());
//output: 1952

console.log(count({ minLength: 5 }));
//output: 1318 

console.log(count({ maxLength: 7 }));
//output: 1649

console.log(count({ minLength: 5, maxLength: 7 }));
//output: 1015
```