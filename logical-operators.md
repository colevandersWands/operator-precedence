# Logical Operators

There are 3 of these exercises.


If you haven't already, do these things before completing the exercises:
1. go back the main README and copy [```are_equal``` function](./README.md).  You'll need this function for the exercises to work.
2. study the [completed examples](./examples-to-study.md)

---


## logical operators 1


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=!%28a%20%26%26%20!b%29%0A!_%0A_%20%26%26%20_%0A!%28_%29%0A%0A)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20!%28a%20%26%26%20!b%29%3B%0A%0Aconst%20op_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20op_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20op_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%20&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("!(a && !b)");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  let step_1 = true, step_2 = true, step_3 = true;

  for ( let i = 0; i < values.length - 1; i++ ) {
    const a = values[i], b = values[i+1];
    const expected = !(a && !b);

    let op_1;
    let st_1;
    are_equal(st_1, expected) ? null : step_1 = false;

    let op_2;
    let st_2;
    are_equal(st_2, expected) ? null : step_2 = false;

    let op_3;
    let st_3;
    are_equal(st_3, expected) ? null : step_3 = false;
  }

  console.log("step 1: ", step_1);
  console.log("step 2: ", step_2);
  console.log("step 3: ", step_3);
}
```

[TOP](#logical-operators)

---


## logical operators 2


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=!!a%20%7C%7C%20!!b%0A!a%0A!_%0A!b%0A!_%0A_%20%7C%7C%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20!!a%20%7C%7C%20!!b%3B%0A%0Aconst%20op_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20op_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20op_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%20%0A%0Aconst%20op_4%20%3D%20%3B%0Aconst%20step_4%20%3D%20%3B%0Aconsole.assert%28step_4%20%3D%3D%3D%20expected,%20%22step_4%22%29%3B%0A%0Aconst%20op_5%20%3D%20%3B%0Aconst%20step_5%20%3D%20%3B%0Aconsole.assert%28step_5%20%3D%3D%3D%20expected,%20%22step_5%22%29%3B%20&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("!!a || !!b");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  let step_1 = true, step_2 = true, step_3 = true;

  for ( let i = 0; i < values.length - 1; i++ ) {
    const a = values[i], b = values[i+1];
    const expected = !!a || !!b;

    let op_1;
    let st_1;
    are_equal(st_1, expected) ? null : step_1 = false;

    let op_2;
    let st_2;
    are_equal(st_2, expected) ? null : step_2 = false;

    let op_3;
    let st_3;
    are_equal(st_3, expected) ? null : step_3 = false;

    let op_4;
    let st_4;
    are_equal(st_4, expected) ? null : step_4 = false;

    let op_5;
    let st_5;
    are_equal(st_5, expected) ? null : step_5 = false;
  }

  console.log("step 1: ", step_1);
  console.log("step 2: ", step_2);
  console.log("step 3: ", step_3);
  console.log("step 4: ", step_4);
  console.log("step 5: ", step_5);
}
```


[TOP](#logical-operators)

---

## logical operators 3


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=a%20%7C%7C%20b%20%26%26%20c%20%7C%7C%20a%0A_%20%26%26%20_%0Aa%20%7C%7C%20_%0A_%20%7C%7C%20a)   
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20a%20%7C%7C%20b%20%26%26%20c%20%7C%7C%20a%3B%0A%0A//%20break%20down%20this%20expression&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("a || b && c || a");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  ; // how many steps are there to validate?

  for ( let i = 0; i < values.length - 2; i++ ) {
    const a = values[i], b = values[i+1], c = values[i+2];
    const expected = a || b && c || a;

    // break down this expression
  }

  // how many steps are there to log?
} 
```
[ast explorer](https://astexplorer.net/#/gist/bc0bac0e8559bf97071c9129a05a28f9/e5fcaa5df8317fb1a45ba1a7866733d96768c463)


[TOP](#logical-operators)

___
___
### <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>
