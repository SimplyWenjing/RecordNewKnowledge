1. Object.create()
	Object.create() 方法创建一个拥有指定原型和若干个指定属性的对象。
	语法：
		Object.create(proto, [ propertiesObject ])
	参数：
		proto：一个对象，作为新创建对象的原型。必须项
		propertiesObject：可选。该参数对象是一组属性与值，该对象的属性名称将是新创建的对象的属性名称，值是属性描述符。注意：该参数对象不能是 undefined，另外只有该对象中自身拥有的可枚举的属性才有效，也就是说该对象的原型链上属性是无效的。
	例子：
		使用Object.create实现类式继承。见new_javascript_knowledge.html.
2. Array.prototype.slice.call() 能将具有length属性的对象转成数组，除了IE下的节点集合（因为ie下的dom对象是以com对象的形式实现的，js对象与com对象不能进行转换） 
	参考：http://www.lai18.com/content/1386795.html
3. navigator.onLine ，是一个属性
	HTML5定义的监测设备是在线还是离线的属性，true为在线，false为离线。
4. String.indexOf();
	indexOf() 方法可返回某个指定的字符串值在字符串中首次出现的位置。之前用到的是只有一个参数，但是这个方法其实可以有第二个参数的。
	语法：	
		stringObject.indexOf(searchvalue,fromindex)
	参数：
		searchvalue:必须，规定需检索的字符串值。
		fromindex：可选，可选的整数参数。规定在字符串中开始检索的位置。它的合法取值是 0 到 stringObject.length - 1。如省略该参数，则将从字符串的首字符开始检索。
	说明：
		该方法将从头到尾地检索字符串 stringObject，看它是否含有子串 searchvalue。开始检索的位置在字符串的 fromindex 处或字符串的开头（没有指定 fromindex 时）。如果找到一个 searchvalue，则返回 searchvalue 的第一次出现的位置。stringObject 中的字符位置是从 0 开始的。
		indexOf() 方法对大小写敏感！
		如果要检索的字符串值没有出现，则该方法返回 -1。

	Array.indexOf() 类似
5. hasOwnProperty()
	object.hasOwnProperty()用于指示一个对象自身(不包括原型链) 是否具有指定名称的属性。如果有，返回true，否则返回false。
	语法：
		object.hasOwnProperty(propertyName )
	参数：	
		object是对象实例，propertyName是属性名。
	说明：
		此方法不会检查对象的原型链中是否存在该属性，该属性只有是对象本身的一个成员才会返回true。想要查看对象(包括原型链)是否具备指定的属性，可以使用in操作符。
		in 返回true ，hasOwnProperty返回false，就是存在于原型中的属性
6. Sting.spilt()
    split()函数用于使用指定分隔符分割字符串，并返回分割后的若干个子字符串组成的数组。即用于把一个字符串分割成字符串数组。
    语法：
    	stringObject.split(separator,howmany);
    参数：
    	separator：必填，字符串或者正则表达式；
    	howmany：可选，Number类型，限制返回的数组中元素个数的最大值。
    说明：
    	（1）如果参数separator是字符串，则split()函数将直接根据该字符串进行分割，而不会试图转换为正则表达式；
    	（2）如果指定的separator参数为空字符串("") ，那么stringObject中的每个字符之间都会被分割。
    	（3）split()方法的返回值为Array类型，返回完成分割后的子字符串数组。子字符串中不会包含separator本身。！！！
7. SSL
8. 类型转换   
   * true==3;//返回的是false，对true进行隐式类型转换，true==1,1==3，返回false
9. 数组的join方法,可以使用不同的分隔符来构建数组字符串。
10. arguments.callee 和 caller的区别   
	* auguments.callee是一个指针，指向拥有这个arguments对象的函数，；
	* caller是函数对象的一个属性，保存着调用当前函数的函数的引用。如果是在全局作用域中调用当前函数，它的值为null。arguments.callee.caller,指向拥有arguments对象的函数
