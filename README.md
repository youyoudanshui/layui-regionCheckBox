# 基于layui的中国省市复选框组件

#### 介绍
基于layui的省市多选解决方案

#### 更新日志
- 2021-02-26
1. 新增动态赋值方法val()
2. 优化代码


#### 使用示例

```
        <div id="regionTest"></div>
```


```
        layui.config({
		  base: '../../../layui_exts/' //配置组件存放的基础目录
		}).extend({
		  regionCheckBox: 'regionCheckBox/regionCheckBox' //定义组件模块名
		}).use(['regionCheckBox'], function(){
		  var $ = layui.$;
		  var regionCheckBox = layui.regionCheckBox;
		  
		  //执行实例
		  var regionTest = regionCheckBox.render({
			elem: '#regionTest',
			name: 'region', // 对应input name
			value: ['北京', '内蒙古', '江西-九江'], // 赋初始值
			width: '550px', // 默认550px
			border: true, // 默认true
			// 初始化完成时执行
			ready: function(){
				// 做些什么
			},
			// 点击复选框时执行
			change: function(result){
				// 做些什么
			}
		  });		  
		});
```

#### 效果截图
![输入图片说明](https://images.gitee.com/uploads/images/2020/0501/162811_9a3fe9c6_5563527.png "微信截图_20200501162506.png")
![输入图片说明](https://images.gitee.com/uploads/images/2020/0501/162825_de117f69_5563527.png "微信截图_20200501162532.png")
![输入图片说明](https://images.gitee.com/uploads/images/2020/0501/162836_74da12f7_5563527.png "微信截图_20200501162544.png")
