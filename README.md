# Operator Precedence

you'll be presented with a single line expression.  your task is to break it into steps according to operator precedence.  The main objective for these exercises is that you become comfortable stepping through and working with complex JS expressions, not that your learn everything about how all operators work.  

Once you become familiar with these exercises you'll find that you're able to complete them just as easily no matter what values you set. 
After mastering them you'll find that you can complete them without even caring what values are going through the expressions!

This is because programming languages are _formal systems_, meaning their text is constructed based on a set of rules.  Once you learn how to manipulate code thinking not about _what it does_ but _how it's structured_ as a text, then you'll be ready to rock and roll.  

__learning objectives__
* which operators exist in JS
* reading this [operator precedence table](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)
* breaking down long expressions (super helpful for debugging, reading & writing code)
* stepping through expressions 
* building nasty debugging skillls
* statements vs. expressions



### Index
* [```are_equal``` function](#are-equal-function)
* [completed examples](./examples-to-study.md)
* exercises
    * [types & casting](./types-and-casting.md)
    * [logical operators](./logical-operators.md)
    * [arithmetic operators](./arithmetic-operators.md)
    * [all primitive operators](./all-primitive-operators.md)
* [resources](#resources)

---

## are equal function

A simple function that behaves almost just like ```===```, with the addition of returning true if both values are ```NaN```.

We suggest you paste this function into your console before completing the exercises.  It'll make things much simpler

```js
function are_equal(x, y) {
  let result;
  if (x !== x) {
    result = y !== y;
  } else if (y !== y) {
    result = false;
  } else {
    return x === y;
  }
  return result;
}
```

[TOP](#operator-precedence)

---



## Resources

* [operator precedence: mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)
* [operator precedence: scripting master](http://www.scriptingmaster.com/javascript/operator-precedence.asp)
* [operator precedence: dummies](https://www.dummies.com/web-design-development/javascript-operator-precedence/)
* expanding expressions: [completed examples](https://github.com/janke-learning/expanding/blob/master/worked-expressions.md), [exercises](https://github.com/janke-learning/expanding/blob/master/exercises-operators-only.md)
* [ast visualizer](https://astexplorer.net/) 
    * explore how JS parses your code and represents operator precedence
    * select to hide everything just above the collapsible tree, makes it readable
    * this tool will be very helpful figuring out order of operations when expanding expressions
        * the deepest operators are executed first, then their parents, ...
    * using this for anything but just expressions will likely be more confusing than helpful
    * this tool doesn't check for syntax errors and doesn't run code, so keep it simple and just copy in the expression. no need for variable declarations


___
___
### <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>
