## call()和apply()方法的区别

call()方法和apply()方法的作用相同，他们的区别在于接收参数的方式不同。对于call()，第一个参数是this值没有变化，变化的是其余参数都直接传递给函数。（在使用call()方法时，传递给函数的参数必须逐个列举出来。使用apply()时，传递给函数的是参数数组）如下代码做出解释：
```
function add(c, d){ 
return this.a + this.b + c + d; 
} 
var o = {a:1, b:3}; 
add.call(o, 5, 7); // 1 + 3 + 5 + 7 = 16 
add.apply(o, [10, 20]); // 1 + 3 + 10 + 20 = 34 
```

## jsonp跨域

只支持get
