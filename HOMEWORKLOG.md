# __HOMEWORKLOG: Initial Instructions__
- Jasmine - test library

## __QUESTIONS__
- ##### NOTE: _QUESTIONS ARE IN ITALICS_
- ##### NOTE: there are no questions past the "REVIEW" section.

### AboutFunctions.js

- "should use lexical scoping to synthesise functions"
  - _why do you add the 3 and the 10 and the 5 and the 5?_
  - _What do you do with the 'param' argument?_
  - _how does lexical scoping synthesise functions?_

- should allow extra function arguments
```
    function () }

    function returnFirstArg(firstArg) }
      return firstArg;
    }

    expect(returnFirstArg("first", "second", "third")).toBe("first");

    function returnSecondArg(firstArg, secondArg) {
      return secondArg;
    }

    expect(returnSecondArg("only give first arg")).toBe(undefined);
```
  - _why is the answer `undefined`?_

### AboutMutibility.js

- I'm not sure about the last two 'fill in the blanks'. _should I write "Penny" or "John"?_

### AboutHigherOrderFunctions.js
_LINK:_ [Part 1: HigherOrderFunctions](https://www.quora.com/What-is-a-simple-explanation-of-higher-order-functions-and-callbacks-in-JavaScript).
- FUNCTIONS PASSED THROUGH OTHER FUNCTIONS ARE CALLED _callback functions_
- .forEach
 - Code
  - `var array = [1, 2, 3];
    (array).forEach(run a function);`
  - `_(numbers).forEach(isEven);`

- it("should use 'forEach' for simple iteration",
 - Answer: `expect(msg).toEqual(falsetruefalse);`
  - _why "falsetruefalse"?_ I thought it would be "2" or [2]
- Q: _Why happens on the `.reduce` line:_

 - it("should use chain() ... .value() to use multiple higher order functions", function() {
 - `.reduce(function (sum, x) { return sum + x })`

### AboutObjects

```
     describe("Properties",

function () {
     var megalomaniac;

     beforeEach(function () {
        megalomaniac = {  mastermind: "Joker", henchwoman: "Harley" };
     });

     it("should confirm objects are collections of properties", function () {
       expect(megalomaniac.mastermind).toBe("Joker");
     });

     it("should confirm that properties are case sensitive", function () {
       expect(megalomaniac.henchwoman).toBe("Harley");
       expect(megalomaniac.henchWoman).toBe(undefined);
     });
   });
```

### AboutApplyWhatWeHaveLearnt

- it("should count the ingredient occurrence (imperative)"
- _Unsure of the purpose of the `|| 0)`_
`(ingredientCount[products[i].ingredients[j]] || 0) + 1;`

======================
======================

## _REVIEW_

#### About Arrays
- `var a = [];
((typeOf(a)).toBe('object')`
 - arrays are 'objects' according to 'typeOf'
- `array[0] = 1` - adds "1" to the first array slot (which is 0)
 - `array.push(3);` - same - puts '3' into last index in an array
 - .slice()
 - `var array = ["Q", "Z", "f", 8](array.slice(0, 1) answer: (["Q"]);`
 - `(array.slice(0, 2)) answer: "Q", "Z", "f"`
- array methods continued
 - `anArray.shift()` // removed index 0
 - `anArray.pop()` // removes last index
 - `anArray.unshift(50)` // goes to index 0
 - `anArray.push("hello")` // adds to end of array

#### AboutFunctions
- internal variables override outer variables
- lexical scoping: `Lexical scoping (sometimes known as static scoping ) is a convention used with many programming languages that sets the scope (range of functionality) of a variable so that it may only be called (referenced) from within the block of code in which it is defined. The scope is determined when the code is compiled.`
- pass functions as value

#### AboutMutibility
- variables inside a constructor and constructor args are private

#### AboutHigherOrderFunctions
- `(array).filter()`
- `(numbers).map( function(x) {
      return x + 1`
- `var numbers = [1, 2, 3];
    var reduction = _(numbers).reduce`...=(6)
    //add all in an array
- `.forEach` to do a simple iteration
- .all
- `.any` - if any is in the array than it's true
- `.range` - should use range to generate an array
- `should use flatten to make nested arrays easy to work with", function() {
      expect(_([ [1, 2], [3, 4] ]).flatten()).toEqual([1, 2, 3, 4]);`
- can _chain_ methods together (.map().reduce/etc.)

#### AboutObjects
- functions that are properties are considered methods
- _this_ refers to an _object_
- shows the key word _in_ to check if a statment is true. `var hasBomb = "theBomb" in megalomaniac;`
- So, `var hasBomb` will be either `true` or `false`.
- in this case it's `true`.
- `hasBomb === true;`
- add 'key: value' properties
 - `megalomaniac.secretary = "Agent Smith";`
 - `megalomaniac.secretary;`
- should use _prototype_ to add to all objects
function Circle(radius)
      {
        this.radius = radius;
      }

      var simpleCircle = new Circle(10);
      var colouredCircle = new Circle(5);
      colouredCircle.colour = "red";

      expect(simpleCircle.colour).toBe(undefined);
      expect(colouredCircle.colour).toBe("red");

      Circle.prototype.describe = function () {
        return "This circle has a radius of: " + this.radius;
      };

      expect(simpleCircle.describe()).toBe("This circle has a radius of: 10");
      expect(colouredCircle.describe()).toBe("This circle has a radius of: 5");

#### AboutInheritance
- can call a method on a derived object
`this.cook = function() {
    return "Mmmm soup!";
  }`
- __should be able to call a method on the derived object__
- __should set constructor parameters on the derived object__
- __should be able to call a method on the base object__
- __should set constructor parameters on the base object__


 #### ABOUTAPPLYWHATWELEARN
- `var a = [];`
- imperitave - list of orders, instructions
- functional - write a function to solve
