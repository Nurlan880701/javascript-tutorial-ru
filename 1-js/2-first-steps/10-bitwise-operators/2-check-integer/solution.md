Один из вариантов такой функции:

```js run
function isInteger(num) {
  return (num ^ 0) === num;
}

alert( isInteger(1) ); // true
alert( isInteger(1.5) ); // false
alert( isInteger(-0.5) ); // false
```

Обратите внимание: `num^0` -- в скобках! Это потому, что приоритет операции `^` очень низкий. Если не поставить скобку, то `===` сработает раньше. Получится `num ^ (0 === num)`, а это уже совсем другое дело.