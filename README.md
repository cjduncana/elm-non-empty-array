# Array.NonEmpty for Elm
[![Build Status](https://travis-ci.org/basti1302/elm-non-empty-array.svg?branch=master)](https://travis-ci.org/basti1302/elm-non-empty-array)

An array that has always at least one element.

````elm
import Array.NonEmpty as NEA exposing (NonEmptyArray)


oneElement : NonEmptyArray
oneElement = NEA.fromElement 13

twoElements : NonEmptyArray
twoElements = NEA.push 42 one

createdFromList : Maybe NonEmptyArray
createdFromList = NEA.fromList ["a", "b", "b"]
````

All functions from core `Array` are available, with the exception of `isEmpty` (which would be an alias for `True`).

In addition, non-empty-array offers an additional function made possible due to the additional constraints:

* `getFirst`: Returns the first element. Since it is known that this element exists, this function does not return a Maybe but the actual element type.


## Tests

The easiest way to run the tests is to install the npm packages `elm-test` and `elm-verify-examples` globally:

```
npm i elm-test -g
npm i elm-verify-examples -g
```

Then, from the project root directory, run

```
elm-verify-examples && elm-test
```

This will require downloading some packages on the first run.

## Version History

* 1.0.0 - 2017-06-30: Initial version.

## License

This library uses the BSD3 License. See LICENSE for more information.
