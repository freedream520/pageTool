pageTool
========

基于jquery和bootstrap的分页插件

预览地址   http://panhb.github.io/pageTool


使用方式

在html中加入如下代码
```html
<ul id="page" class="pagination" ></ul>
```

在javascript中

初始化组件
```js
PageTool.init({
		//一页显示多少条记录
		pageSize:7,
		//页码最大值
		totalCount:100,
		//页码最多显示多少
		pageMax:10,
		//点击页码响应函数名
		funcName:"select",
		//点击前一页响应函数名
		funcPreviousName:"previous",
		//点击下一页响应函数名
		funcNextName:"next",
		//当前页码是否可点击  true为可点击
		clickFlag:false
	},function(){});
```


获取当前选中页码
```js
PageTool.getCurrentPage()
```


设置选中页码
```js
PageTool.setPage(index,function(){});
```


推荐实现方式
```js
PageTool.init({
		totalCount:100,
		pageSize:7, 
		pageMax:10 
	},function(){});
	
function select(index){
	PageTool.setPage(index,function(){});
}

function previous(){
	select(PageTool.getCurrentPage()-1);
}

function next(){
	select(PageTool.getCurrentPage()+1);
}
```

