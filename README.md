# ECMAScript Parsing Quartets Collection 
This Quartet Collection provides you with some Quartets for parsing and understanding portion of ECMAScript 2016.  By using these Quartets you get the benefit of easier code to maintain in situations that you just wanna find var names or likewise situations.

## Quartets
### String.quartet
This Quartet finds all of the string literals. For ECMAScript's new string system:

```JavaScript
`... ${ 1 } ... ${ "hey" } ...`
``` 

It matches the values of Interpolations.

### Storage Names
This Quartet finds all of the identifiers of type: `const`, `var` and `let`. Also node includes like:

```JavaScript
const { a, b, c } = require('something'); 
```

Are possible.

Each match includes group matches. The first one is the type ( `cost` | `var` | `let` ) then there is the identifier / identifiers name(s). So for example `const hello = 2` returns [ `const`, `hello` ]. `let { a, b, c } = require('hello')` returns [ `let`, `a`, `b`, `c` ].

