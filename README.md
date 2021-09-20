# 基于layui的中国省市复选框组件

#### 介绍
基于layui的省市多选解决方案

#### 更新日志
- 2021-09-20
1. 调整数据结构，支持复选框选项值自定义
- 2021-03-11
1. 支持字符串赋值，多个值用“,”隔开
- 2021-02-26
1. 新增动态赋值方法val()
2. 新增支持实例化多个
3. 新增重载方法
4. 优化代码

#### 参数列表
| 参数     | 类型           | 说明                       | 示例值             |
|--------|--------------|--------------------------|-----------------|
| elem   | String       | 指定容器的选择器，必填              | #demo           |
| name   | String       | checkbox name属性值         | region          |
| data   | Array        | 设置checkbox选项值和显示的文字，不设置则使用预设选项 | 参考region.json和demo页 |
| all    | Array        | 全选框值和显示的文字，若为null则不显示全选框 | ['all', '全部']   |
| value  | Array/String | 赋初始值                     | ['北京', '云南-昆明']/'北京,云南-昆明' |
| width  | String       | 容器宽度，默认550px             | 400px           |
| border | Boolean      | 是否显示边框，默认true            | false           |

#### 回调
| 方法名                        | 备注       |
|----------------------------|----------|
| ready: function(){}        | 初始化完成时触发 |
| change: function(result){} | 点击复选框时触发 |

#### 基础方法
| 方法名                        | 备注       |
|----------------------------|----------|
| regionCheckBox.render(options)          | 渲染 |
| regionCheckBox.val(value)          | 赋值 |
| regionCheckBox.reload(options)     | 重载 |

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
			value: ['北京', '内蒙古', '江西-九江'], // 赋初始值，'北京,内蒙古,江西-九江'也可以
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
