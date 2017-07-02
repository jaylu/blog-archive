title: HTML5 打牌计分器
date: 2015-08-22 12:14:46
tags: [html5,angular,css]
---

<div style="background:lightcoral; text-align: center; "><a style="font-family: Helvetica Neue, Helvetica, Arial;font-weight: 300; color:white; font-size: large;" 
href="http://bigtwo.duapp.com" target="_blank" rel="external">点击打开</a>
</div>


### 它是什么

这是一个打牌的计分器，用户可以在每一盘结束后输入每人当前剩余的牌数，它会自动统计每人的得分状态。

以下是一些截图

![添加纪录](app_1.png) ![删除记录](app_2.png)

### 怎样使用

#### 更改玩家的名字： 

* 点击左上角的图标，玩家的名字就会变成可编辑的状态
* 更改玩家的名字
* 再次点击左上角的图标，完成编辑

#### 输入每一盘的结果

* 点击“添加记录”， 输入框会自动展开，通过数字按键输入对应玩家的剩余牌数
* 通过点击来移动光标
* 只有在当前输入行有效(1.所有玩家已经录入 2.有一个录入为0存在)的时候，确定按纽才会生效，通过点击“确定”增加当前记录
* 点击“取消”会取消整行的输入并返回。

#### 删除记录

* 在记录行上向左划动，会出现“删除”按纽，点击则可以删除记录
* 假如不想删除，向右划动，“删除”按纽会消失

### 技术细节

* 主要用Angularjs实现，手写的CSS实现页面布局，还有一些CSS3的动画效果
* node.js＋express作为静态服务器, 部署在百度云的app engine上 


