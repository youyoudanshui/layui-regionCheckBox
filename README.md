# 基于layui的中国省市复选框组件

#### 介绍
基于layui的省市多选解决方案

#### 软件架构
软件架构说明


#### 使用示例


```
                layui.config({
		  base: '../../../layui_exts/' //配置组件存放的基础目录
		}).extend({
		  regionCheckBox: 'regionCheckBox/regionCheckBox' //定义组件模块名
		}).use(['regionCheckBox'], function(){
		  var $ = layui.$;
		  var regionCheckBox = layui.regionCheckBox;
		  
		  //执行实例
		  regionCheckBox.render({
			elem: '#regionTest',
			name: 'region', //input name
			value: ['北京', '内蒙古', '江西-九江'], //赋初始值
			width: '550px', //默认550px
			border: true, //默认true
			ready: function(){ //初始化完成时执行
				//做些什么
			},
			change: function(result){ //点击复选框时执行
				//做些什么
			}
		  });
```

#### 效果截图
![输入图片说明](https://images.gitee.com/uploads/images/2020/0501/162713_b6e03da0_5563527.png "微信截图_20200501162544.png")
