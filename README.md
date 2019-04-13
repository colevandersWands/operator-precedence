# Operator Precedence

you'll be presented with a single line expression.  your task is to break it into steps according to operator precedence.  The main objective for these exercises is that you become comfortable stepping through and working with complex JS expressions, not that your learn everything about how all operators work.  Understanding implicit coercion is very important but will be covered in depth later on.  

learning objectives
* which operators exist in JS
* operator precedence
* breaking down long expressions (super helpful for debugging)
* statements vs. expressions



### Index
* [completed examples](#completed-examples)
* exercises
  * [types & casting](#types-and-casting)
  * [logical operators](#logical-operators)
  * [number operators](#number-operators)
  * [in-place operators](#in-place-operators)
  * [all primitive operators](#all-primitive-operators)
* [resources](#resources)

---

## Completed Examples

### 1

[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20Number%28Boolean%28String%28a%29%29%29%3B%0A%0Aconst%20val_1%20%3D%20String%28a%29%3B%0Aconst%20step_1%20%3D%20Number%28Boolean%28val_1%29%29%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20Boolean%28val_1%29%3B%0Aconst%20step_2%20%3D%20Number%28val_2%29%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20Number%28val_2%29%3B%0Aconst%20step_3%20%3D%20val_3%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
[parsonized](https://janke-learning.github.io/parsonizer/?snippet=Number%28Boolean%28String%28a%29%29%29%0AString%28_%29%0ABoolean%28_%29%0ANumber%28_%29)
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = ;

  const expected = Number(Boolean(String(a)));

  const val_1 = String(a);
  const step_1 = Number(Boolean(val_1));
  console.assert(step_1 === expected, "step_1");

  const val_2 = Boolean(val_1);
  const step_2 = Number(val_2);
  console.assert(step_2 === expected, "step_2");

  const val_3 = Number(val_2);
  const step_3 = val_3;
  console.assert(step_3 === expected, "step_3");
}
```

### 2

[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20%28a%20%2B%20b%29%20%3D%3D%20%28a%20%3C%20c%29%3B%0A%0Aconst%20val_1%20%3D%20a%20%2B%20b%3B%0Aconst%20step_1%20%3D%20val_1%20%3D%3D%20%28a%20%3C%20c%29%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20a%20%3C%20c%3B%0Aconst%20step_2%20%3D%20val_1%20%3D%3D%20val_2%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20val_1%20%3D%3D%20val_2%3B%0Aconst%20step_3%20%3D%20val_3%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
[parsonized](https://janke-learning.github.io/parsonizer/?snippet=%28a%20%2B%20b%29%20%3D%3D%20%28a%20%3C%20c%29%0A_%20%2B%20_%0A_%20%3C%20_%0A_%20%3D%3D%20_%0A%0A%0A%0A)
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = , b = , c = ;

  const expected = (a + b) == (a < c);

  const val_1 = a + b;
  const step_1 = val_1 == (a < c);
  console.assert(step_1 === expected, "step_1");

  const val_2 = a < c;
  const step_2 = val_1 == val_2;
  console.assert(step_2 === expected, "step_2");

  const val_3 = val_1 == val_2;
  const step_3 = val_3;
  console.assert(step_3 === expected, "step_3");
}
```

### 3

[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20b%20%26%26%20typeof%20a%20%3D%3D%3D%20'string'%3B%0A%0Aconst%20val_1%20%3D%20typeof%20a%3B%0Aconst%20step_1%20%3D%20val_1%20%3D%3D%3D%20'string'%20%26%26%20b%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20val_1%20%3D%3D%3D%20'string'%3B%0Aconst%20step_2%20%3D%20val_2%20%26%26%20b%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20val_2%20%26%26%20b%3B%0Aconst%20step_3%20%3D%20val_3%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
[parsonized](https://janke-learning.github.io/parsonizer/?snippet=b%20%26%26%20typeof%20a%20%3D%3D%3D%20'string'%0Atypeof%20_%0A_%20%3D%3D%3D%20'string'%0A_%20%26%26%20_)
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = , b = ;

  const expected = b && typeof a === 'string';

  const val_1 = typeof a;
  const step_1 = val_1 === 'string' && b;
  console.assert(step_1 === expected, "step_1");

  const val_2 = val_1 === 'string';
  const step_2 = val_2 && b;
  console.assert(step_2 === expected, "step_2");

  const val_3 = val_2 && b;
  const step_3 = val_3;
  console.assert(step_3 === expected, "step_3");
}
```
[short-circuiting - an advanced gotcha](https://codeburst.io/javascript-what-is-short-circuit-evaluation-ff22b2f5608c)

### 4

[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20%28%20a%20%3E%20Number%28b%29%20%29%20%7C%7C%20String%28c%29%3B%0A%0Aconst%20val_1%20%3D%20Number%28b%29%3B%0Aconst%20step_1%20%3D%20%28%20a%20%3E%20val_1%20%29%20%7C%7C%20String%28c%29%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20a%20%3E%20val_1%3B%0Aconst%20step_2%20%3D%20%28%20val_2%20%29%20%7C%7C%20String%28c%29%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20String%28c%29%3B%0Aconst%20step_3%20%3D%20val_2%20%7C%7C%20val_3%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%0A%0Aconst%20val_4%20%3D%20val_2%20%7C%7C%20val_3%3B%0Aconst%20step_4%20%3D%20val_4%3B%0Aconsole.assert%28step_4%20%3D%3D%3D%20expected,%20%22step_4%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
[parsonized](https://janke-learning.github.io/parsonizer/?snippet=%28%20a%20%3E%20Number%28b%29%20%29%20%7C%7C%20String%28c%29%0ANumber%28_%29%0A_%20%3E%20_%0AString%28_%29%0A_%20%7C%7C%20_)
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = , b = , c = ;

  const expected = ( a > Number(b) ) || String(c);

  const val_1 = Number(b);
  const step_1 = ( a > val_1 ) || String(c);
  console.assert(step_1 === expected, "step_1");

  const val_2 = a > val_1;
  const step_2 = ( val_2 ) || String(c);
  console.assert(step_2 === expected, "step_2");

  const val_3 = String(c);
  const step_3 = val_2 || val_3;
  console.assert(step_3 === expected, "step_3");

  const val_4 = val_2 || val_3;
  const step_4 = val_4;
  console.assert(step_4 === expected, "step_4");
}
```
[short-circuiting - an advanced gotcha](https://codeburst.io/javascript-what-is-short-circuit-evaluation-ff22b2f5608c)



[TOP](#operator-precedence)

---

## Exercises

## Types and Casting

### types & casting 1

[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20typeof%20a%20%3D%3D%3D%20typeof%20b%3B%0A%0Aconst%20val_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
[parsonized](https://janke-learning.github.io/parsonizer/?snippet=typeof%20a%20%3D%3D%3D%20typeof%20b%0Atypeof%20a%0Atypeof%20b%0A_%20%3D%3D%3D%20_)
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = , b = ;

  const expected = typeof a === typeof b;

  const val_1 = ;
  const step_1 = ;
  console.assert(step_1 === expected, "step_1");

  const val_2 = ;
  const step_2 = ;
  console.assert(step_2 === expected, "step_2");

  const val_3 = ;
  const step_3 = ;
  console.assert(step_3 === expected, "step_3");
}
```

### types & casting 2

[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20Boolean%28a%29%20!%3D%3D%20Boolean%28b%29%3B%0A%0Aconst%20val_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%20&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
[parsonized](https://janke-learning.github.io/parsonizer/?snippet=Boolean%28a%29%20!%3D%3D%20Boolean%28b%29%0ABoolean%28a%29%0ABoolean%28b%29%0A_%20!%3D%3D%20_)
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = , b = ;

  const expected = Boolean(a) !== Boolean(b);

  const val_1 = ;
  const step_1 = ;
  console.assert(step_1 === expected, "step_1");

  const val_2 = ;
  const step_2 = ;
  console.assert(step_2 === expected, "step_2");

  const val_3 = ;
  const step_3 = ;
  console.assert(step_3 === expected, "step_3"); 
}
```

## types & casting 3

[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20Boolean%28b%29%20%3D%3D%3D%20Boolean%28Number%28a%29%29%3B%0A%0Aconst%20val_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%0A%0Aconst%20val_4%20%3D%20%3B%0Aconst%20step_4%20%3D%20%3B%0Aconsole.assert%28step_4%20%3D%3D%3D%20expected,%20%22step_4%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
[parsonized](https://janke-learning.github.io/parsonizer/?snippet=Boolean%28b%29%20%3D%3D%3D%20Boolean%28Number%28a%29%29%0ABoolean%28b%29%0ANumber%28a%29%0ABoolean%28_%29%0A_%20%3D%3D%3D%20_)
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = , b = ;

  const expected = Boolean(b) === Boolean(Number(a));

  const val_1 = ;
  const step_1 = ;
  console.assert(step_1 === expected, "step_1");

  const val_2 = ;
  const step_2 = ;
  console.assert(step_2 === expected, "step_2");

  const val_3 = ;
  const step_3 = ;
  console.assert(step_3 === expected, "step_3");

  const val_4 = ;
  const step_4 = ;
  console.assert(step_4 === expected, "step_4");
}
```

## Resources

* [operator precedence: mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)
* [operator precedence: dummies](https://www.dummies.com/web-design-development/javascript-operator-precedence/)

___
___
### <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>
