[![Codacy Badge](https://api.codacy.com/project/badge/Grade/fb410b8b15b44a878ce67d5e4f893bea)](https://app.codacy.com/app/treadpit/wx_selectArea?utm_source=github.com&utm_medium=referral&utm_content=treadpit/wx_selectArea&utm_campaign=badger)
[![Dependency status](https://img.shields.io/david/treadpit/wx_selectArea.svg)](https://david-dm.org/treadpit/wx_selectArea)
[![Build Status](https://travis-ci.org/treadpit/wx_selectArea.svg?branch=master)](https://travis-ci.org/treadpit/wx_selectArea)
[![GitHub issues](https://img.shields.io/github/issues/treadpit/wx_selectArea.svg?style=flat-square)](https://github.com/treadpit/wx_selectArea/issues)

# wx_selectArea

地址联动选择器采用微信小程序的 `picker-view` 组件
### 模板引入

提供 `template` [模板引入](https://mp.weixin.qq.com/debug/wxadoc/dev/framework/view/wxml/template.html)

1. 引入`wxml`及`wxss`
```xml
// example.wxml
<import src="../../template/index.wxml"/>
<template is="areaPicker" data="{{...areaPicker}}" />

// example.wxss
@import '../../template/index.wxss';
```
2. 组件初始化
```js
// example.js

import initAreaPicker, { getSelectedAreaData } from '../../template/index';
Page({
	onShow: () => {
		initAreaPicker();
	},
	getSelecedData() {
		console.table(getSelectedAreaData()); // 提供`getSelectedAreaData`方法，返回当前选择的省市区信息组成的数组
	}
});

```

### 截图

<img src="https://raw.githubusercontent.com/treadpit/wx_selectArea/develop/screenshot/devtool_screenshot.png" width="1000px">

<img src="https://github.com/treadpit/wx_selectArea/blob/master/screenshot/182245dl7zwrbc5rl2g7ls.gif" width="380px">

#### 旧版

> 小程序不支持 `picker-view` 组件时，用 `scroll-view` 模拟的联动选择器（不再维护）

<img src="https://github.com/treadpit/wx_selectArea/blob/master/screenshot/154906d8z81rtbrh4t4ith.gif" width="380px">

欢迎反馈...
