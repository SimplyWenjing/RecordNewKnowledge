1、 Object.create()
	Object.create() 方法创建一个拥有指定原型和若干个指定属性的对象。
	语法：
		Object.create(proto, [ propertiesObject ])
	参数：
		proto：一个对象，作为新创建对象的原型。必须项
		propertiesObject：可选。该参数对象是一组属性与值，该对象的属性名称将是新创建的对象的属性名称，值是属性描述符。注意：该参数对象不能是 undefined，另外只有该对象中自身拥有的可枚举的属性才有效，也就是说该对象的原型链上属性是无效的。
	例子：
		使用Object.create实现类式继承。见new_javascript_knowledge.html.
