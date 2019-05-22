ES6 study
=========

1.
	var 申明的变量为全局变量

	let 申明的变量为局部变量，只在申明变量当前块状内生效

	let的存在会使其所申明的块状区域出现暂时性锁区现象

	例： 
```javascript
	var tmp = 11;

	if(true){

		tmp = 22;

		let tmp;

	}
```

	此时会报错，该块状区域被锁定，tmp未定义；

2.
	const 用法与let相同，区别是const定义的变量的值是常量，且其变量已经赋值就不能再次赋值，否则将会报错
	
	另const定义的变量必须立即赋值，不可等之后再赋值，否则也会报错

	例：
```javascript
		var name = 'lisi';

		const name = 'xioa';//此时也会报错

		const obj = {};

		obj.name = 'name';
		
		obj.pasword = '123456';
````
		此时不会报错，可以给其申明的对象赋值，

		但若 obj = {} 这样直接赋值另一个变量时则会报错 

3.
	解构：

		左边的变量会按顺序赋予右边的值  如： let [a,b,c] = [1,2,3]; 结果为 a=1,b=2,c=3;

		也可使用 let {round,floor,ceil} = Math; 简化函数