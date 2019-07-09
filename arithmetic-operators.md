# Arithmetic Operators

There are 3 of these exercises.


If you haven't already, do these things before completing the exercises:
1. go back the main README and copy [```are_equal``` function](./README.md).  You'll need this function for the exercises to work.
2. study the [completed examples](./examples-to-study.md)

---

## arithmetic operators 1


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=-%28a%20%2B%20b%29%20*%20c%0A_%20%2B%20_%0A-%28_%29%0A_%20*%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%200,%201,%20-1,%20NaN,%20Infinity,%20.5,%20-0.0,%201e3,%201e-3,%20999e305,%20999e306%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20-%28a%20%2B%20b%29%20*%20c%3B%0A%0Aconst%20op_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20op_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20op_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%20&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("-(a + b) * c");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  ; // how many steps are there to validate?

  for ( let i = 0; i < values.length - 2; i++ ) {
    const a = values[i], b = values[i+1], c = values[i+2];
    const expected = -(a + b) * c;

    // break down this expression
  }

  // how many steps are there to log?
} 
```

> [scientific notation](http://www.java2s.com/Tutorials/Javascript/Javascript_Tutorial/Data_Type/How_to_write_Scientific_notation_literal_in_Javascript.htm)

[TOP](#arithmetic-operators)

---

## arithmetic operators 2


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=a%20**%20b%20%2F%20%2Bc%0A%2B_%0A_%20**%20_%0A_%20%2F%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%200,%201,%20-1,%20NaN,%20Infinity,%20.5,%20-0.0,%201e3,%201e-3,%20999e305,%20999e306%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20a%20**%20b%20/%20%2Bc%3B%0A%0A//%20break%20down%20this%20expression%20&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("a ** b / +c");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  ; // how many steps are there to validate?

  for ( let i = 0; i < values.length - 2; i++ ) {
    const a = values[i], b = values[i+1], c = values[i+2];
    const expected = a ** b / +c;

    // break down this expression
  }

  // how many steps are there to log?
} 
```

[TOP](#arithmetic-operators)

---

## arithmetic operators 3


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=b%20%25%20c%20-%20a%20**%20c%20%2F%20b%0A_%20**%20_%0A_%20%2F%20_%0A_%20%25%20_%0A_%20-%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%200,%201,%20-1,%20NaN,%20Infinity,%20.5,%20-0.0,%201e3,%201e-3,%20999e305,%20999e306%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20b%20%25%20c%20-%20a%20**%20c%20/%20b%3B%0A%0A//%20break%20down%20this%20expression&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("b % c - a ** c / b");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  ; // how many steps are there to validate?

  for ( let i = 0; i < values.length - 3; i++ ) {
    const a = values[i], b = values[i+1], c = values[i+2], d = values[i+3];
    const expected = b % c - a ** c / b;

    // break down this expression
  }

  // how many steps are there to log?
} 
```

[TOP](#arithmetic-operators)

___
___
## <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>
