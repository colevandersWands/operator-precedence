# All Primitive Operators


There are 5 of these exercises.


If you haven't already, do these things before completing the exercises:
1. go back the main README and copy [```are_equal``` function](./README.md).  You'll need this function for the exercises to work.
2. study the [completed examples](./examples-to-study.md)

---

## all primitive operators 1


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=a%20%25%20b%20%7C%7C%20!!a%0A_%20%25%20_%0A!a%0A!_%0A_%20%7C%7C%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%200,%201,%20-1,%20NaN,%20Infinity,%20.5,%20-0.0,%201e3,%201e-3,%20999e305,%20999e306%0A%20%200,%203%0A%20%201,%203%0A%20%202,%203%0A%20%203,%203%0A%20%204,%203%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20a%20%25%20b%20%7C%7C%20!!a%3B%0A%0A//%20break%20down%20this%20expression&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("a % b || !!a");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  ; // how many steps are there to validate?

  for ( let i = 0; i < values.length - 1; i++ ) {
    const a = values[i], b = values[i+1];
    const expected = a % b || !!a;

    // break down this expression
  }

  // how many steps are there to log?
} 
```

[TOP](#all-primitive-operators)

---

## all primitive operators 2


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=typeof%20a%20%3D%3D%3D%20'number'%20%2B%20a%0Atypeof%20_%0A_%20%3D%3D%3D%20_%0A_%20%2B%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%200,%201,%20-1,%20NaN,%20Infinity,%20.5,%20-0.0,%201e3,%201e-3,%20999e305,%20999e306%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20typeof%20a%20%3D%3D%3D%20'number'%20%2B%20a%3B%0A%0A//%20break%20down%20this%20expression&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("typeof a === 'number' + a");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  ; // how many steps are there to validate?

  for ( let i = 0; i < values.length; i++ ) {
    const a = values[i];
    const expected = typeof a === 'number' + a;

    // break down this expression
  }

  // how many steps are there to log?
} 
```

[TOP](#all-primitive-operators)

---


## all primitive operators 3


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=!!%2Ba%20%3D%3D%3D%20Boolean%28a%29%0A%2B_%0A!_%0A!_%0ABoolean%28_%29%0A_%20%3D%3D%3D%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20!!%2Ba%20%3D%3D%3D%20Boolean%28a%29%3B%0A%0A//%20break%20down%20this%20expression&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("!!+a === Boolean(a)");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  ; // how many steps are there to validate?

  for ( let i = 0; i < values.length; i++ ) {
    const a = values[i];
    const expected = !!+a === Boolean(a);

    // break down this expression
  }

  // how many steps are there to log?
}
```

[TOP](#all-primitive-operators)

---

## all primitive operators 4

```js
{ console.log("a ** a < b % b && c !== c");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  ; // how many steps are there to validate?

  for ( let i = 0; i < values.length - 2; i++ ) {
    const a = values[i], b = values[i+1], c = values[i+2];
    const expected = a ** a < b % b && c !== c;

    // break down this expression
  }

  // how many steps are there to log?
}
```

[TOP](#all-primitive-operators)

---

## all primitive operators 5

```js
{ console.log("!+(!!a++b%a)");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  ; // how many steps are there to validate?

  for ( let i = 0; i < values.length - 1; i++ ) {
    const a = values[i], b = values[i+1];
    const expected = !+(!!a++b%a);

    // break down this expression
  }

  // how many steps are there to log?
}
```

[TOP](#all-primitive-operators)


___
___
### <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>

