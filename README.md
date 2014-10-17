pageTool
========

基于jquery和bootstrap的分页插件

预览地址   http://panhb.github.io/pageTool


使用方式

在html中加入如下代码
```html
<ul id="page" class="pagination" ></ul>
</div>
```

在javascript中

初始化组件
```js
PageTool.init({
		totalCount:100,
		pageSize:7, 
		pageMax:10 
	},function(){
	});
```

获取当前选中页码
```js
PageTool.getCurrentPage()
```

设置选中页码
```js
PageTool.setPage(index,function(){
});
```

推荐实现方式
```js
PageTool.init({
		totalCount:100,
		pageSize:7, 
		pageMax:10 
	},function(){
	});
	
function select(index){
	PageTool.setPage(index,function(){
	});
}

function previous(){
	select(PageTool.getCurrentPage()-1);
}

function next(){
	select(PageTool.getCurrentPage()+1);
}
```

