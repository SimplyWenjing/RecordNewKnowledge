### 1、margin折叠问题
	如果一个元素嵌套在另一个元素中，如果外面元素有边框，那么二者的外边距不会折叠，如果没有边框，则二者的上外边距会折叠
### 2、内联元素对float会围绕
	当页面上有float元素的时候，对内联元素进行定位时，内联元素会考虑浮动元素的边界，因此会围绕着浮动元素。
### 3、清除浮动的方法    
	* 额外标签法，设置clear:both;
	* 使用after伪类 
	div:after{
		content:".";
		height:0;
		visibility:hidden;
		display:block;
		clear:both;
	}
	* 设置overflow:hidden