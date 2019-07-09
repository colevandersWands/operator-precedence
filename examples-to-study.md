# Examples to Study

some completed examples you can study before moving on to the exercises.

If you haven't already, go back the main README and copy [```are_equal``` function](./README.md).  You'll need this function for the exercises to work.

### examples
- [one](#1)
- [two](#2)
- [three](#3)
- [four](#4)
- [five](#5)

---

## 1


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=Number%28Boolean%28String%28a%29%29%29%0AString%28_%29%0ABoolean%28_%29%0ANumber%28_%29)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20Number%28Boolean%28String%28a%29%29%29%3B%0A%0Aconst%20op_1%20%3D%20String%28a%29%3B%0Aconst%20step_1%20%3D%20Number%28Boolean%28op_1%29%29%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20op_2%20%3D%20Boolean%28op_1%29%3B%0Aconst%20step_2%20%3D%20Number%28op_2%29%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20op_3%20%3D%20Number%28op_2%29%3B%0Aconst%20step_3%20%3D%20op_3%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("Number(Boolean(String(a)))");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  let step_1 = true, step_2 = true, step_3 = true;

  for ( let i = 0; i < values.length; i++ ) {
    const a = values[i];
    const expected = Number(Boolean(String(a)));

    const op_1 = String(a);
    const st_1 = Number(Boolean(op_1));
    are_equal(st_1, expected) ? null : step_1 = false;

    const op_2 = Boolean(op_1);
    const st_2 = Number(op_2);
    are_equal(st_2, expected) ? null : step_2 = false;

    const op_3 = Number(op_2);
    const st_3 = op_3;
    are_equal(st_3, expected) ? null : step_3 = false;
  }

  console.log("step 1: ", step_1);
  console.log("step 2: ", step_2);
  console.log("step 3: ", step_3);
}
```


[TOP](#examples-to-study)

---

## 2

[parsonized](https://janke-learning.github.io/parsonizer/?snippet=%28a%20%2B%20b%29%20%3D%3D%20%28a%20%3C%20c%29%0A_%20%2B%20_%0A_%20%3C%20_%0A_%20%3D%3D%20_%0A%0A%0A%0A)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20%28a%20%2B%20b%29%20%3D%3D%20%28a%20%3C%20c%29%3B%0A%0Aconst%20op_1%20%3D%20a%20%2B%20b%3B%0Aconst%20step_1%20%3D%20op_1%20%3D%3D%20%28a%20%3C%20c%29%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20op_2%20%3D%20a%20%3C%20c%3B%0Aconst%20step_2%20%3D%20op_1%20%3D%3D%20op_2%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20op_3%20%3D%20op_1%20%3D%3D%20op_2%3B%0Aconst%20step_3%20%3D%20op_3%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  

```js
{ console.log("(a + b) == (a < c)");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  let step_1 = true, step_2 = true, step_3 = true;

  for ( let i = 0; i < values.length - 2; i++ ) {
    const a = values[i], b = values[i+1], c = values[i+2];
    const expected = (a + b) == (a < c);

    const op_1 = a + b;
    const st_1 = op_1 == (a < c);
    are_equal(st_1, expected) ? null : step_1 = false;

    const op_2 = a < c;
    const st_2 = op_1 == op_2;
    are_equal(st_2, expected) ? null : step_2 = false;

    const op_3 = op_1 == op_2;
    const st_3 = op_3;
    are_equal(st_3, expected) ? null : step_3 = false;
  }

  console.log("step 1: ", step_1);
  console.log("step 2: ", step_2);
  console.log("step 3: ", step_3);
}
```

[TOP](#examples-to-study)

---

## 3


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=b%20%26%26%20typeof%20a%20%3D%3D%3D%20'string'%0Atypeof%20_%0A_%20%3D%3D%3D%20'string'%0A_%20%26%26%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20b%20%26%26%20typeof%20a%20%3D%3D%3D%20'string'%3B%0A%0Aconst%20op_1%20%3D%20typeof%20a%3B%0Aconst%20step_1%20%3D%20b%20%26%26%20op_1%20%3D%3D%3D%20'string'%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20op_2%20%3D%20op_1%20%3D%3D%3D%20'string'%3B%0Aconst%20step_2%20%3D%20b%20%26%26%20op_2%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20op_3%20%3D%20b%20%26%26%20op_2%3B%0Aconst%20step_3%20%3D%20op_3%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=1&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("b && typeof a === 'string'");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  let step_1 = true, step_2 = true, step_3 = true;

  for ( let i = 0; i < values.length - 1; i++ ) {
    const a = values[i], b = values[i+1];
    const expected = b && typeof a === 'string';

    const op_1 = typeof a;
    const st_1 = b && op_1 === 'string';
    are_equal(st_1, expected) ? null : step_1 = false;

    const op_2 = op_1 === 'string';
    const st_2 = b && op_2;
    are_equal(st_2, expected) ? null : step_2 = false;

    const op_3 = b && op_2;
    const st_3 = op_3;
    are_equal(st_3, expected) ? null : step_3 = false;
  }

  console.log("step 1: ", step_1);
  console.log("step 2: ", step_2);
  console.log("step 3: ", step_3);
}
```

[short-circuiting - an advanced gotcha](https://github.com/janke-learning/expanding/blob/master/worked-short-circuiting.md)


[TOP](#examples-to-study)

---

## 4


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=%28b%20%26%26%20typeof%20a%29%20%3D%3D%3D%20'string'%0Atypeof%20_%0A_%20%26%26%20_%0A_%20%3D%3D%3D%20'string')  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20%28b%20%26%26%20typeof%20a%29%20%3D%3D%3D%20'string'%3B%0A%0Aconst%20op_1%20%3D%20typeof%20a%3B%0Aconst%20step_1%20%3D%20op_1%20%3D%3D%3D%20'string'%20%26%26%20b%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20op_2%20%3D%20b%20%26%26%20op_1%3B%0Aconst%20step_2%20%3D%20op_2%20%3D%3D%3D%20'string'%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20op_3%20%3D%20op_2%20%3D%3D%3D%20'string'%3B%0Aconst%20step_3%20%3D%20op_3%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("(b && typeof a) === 'string'");

  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  let step_1 = true, step_2 = true, step_3 = true;

  for ( let i = 0; i < values.length - 1; i++ ) {
    const a = values[i], b = values[i+1];
    const expected = (b && typeof a) === 'string';

    const op_1 = typeof a;
    const st_1 = (b && op_1) === 'string';
    are_equal(st_1, expected) ? null : step_1 = false;

    const op_2 = b && op_1;
    const st_2 = op_2 === 'string';
    are_equal(st_2, expected) ? null : step_2 = false;

    const op_3 = op_2 === 'string';
    const st_3 = op_3;
    are_equal(st_3, expected) ? null : step_3 = false;
  }

  console.log("step 1: ", step_1);
  console.log("step 2: ", step_2);
  console.log("step 3: ", step_3);
}
```


[TOP](#examples-to-study)

---

## 5


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=%28%20a%20%3E%20Number%28b%29%20%29%20%7C%7C%20String%28c%29%0ANumber%28_%29%0A_%20%3E%20_%0AString%28_%29%0A_%20%7C%7C%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20%28%20a%20%3E%20Number%28b%29%20%29%20%7C%7C%20String%28c%29%3B%0A%0Aconst%20op_1%20%3D%20Number%28b%29%3B%0Aconst%20step_1%20%3D%20%28%20a%20%3E%20op_1%20%29%20%7C%7C%20String%28c%29%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20op_2%20%3D%20a%20%3E%20op_1%3B%0Aconst%20step_2%20%3D%20%28%20op_2%20%29%20%7C%7C%20String%28c%29%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20op_3%20%3D%20String%28c%29%3B%0Aconst%20step_3%20%3D%20op_2%20%7C%7C%20op_3%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_3%22%29%3B%0A%0Aconst%20op_4%20%3D%20op_2%20%7C%7C%20op_3%3B%0Aconst%20step_4%20%3D%20op_4%3B%0Aconsole.assert%are_equal(28ste,20)%3D%3D%3D%20expected,%20%22step_4%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{ console.log("( a > Number(b) ) || String(c)");
  const values = ["", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity];
  let step_1 = true, step_2 = true, step_3 = true, step_4 = true;

  for ( let i = 0; i < values.length - 2; i++ ) {
    const a = values[i], b = values[i+1], c = values[i+2];
    const expected = ( a > Number(b) ) || String(c);

    const op_1 = Number(b);
    const st_1 = ( a > op_1 ) || String(c);
    are_equal(st_1, expected) ? null : step_1 = false;

    const op_2 = a > op_1;
    const st_2 = ( op_2 ) || String(c);
    are_equal(st_2, expected) ? null : step_2 = false;

    const op_3 = String(c);
    const st_3 = op_2 || op_3;
    are_equal(st_3, expected) ? null : step_3 = false;

    const op_4 = op_2 || op_3;
    const st_4 = op_4;
    are_equal(st_4, expected) ? null : step_4 = false;
  }

  console.log("step 1: ", step_1);
  console.log("step 2: ", step_2);
  console.log("step 3: ", step_3);
  console.log("step 4: ", step_4);
}
```


[short-circuiting - an advanced gotcha](https://codeburst.io/javascript-what-is-short-circuit-evaluation-ff22b2f5608c)



[TOP](#examples-to-study)


___
___
## <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>
