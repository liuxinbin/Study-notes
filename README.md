# 学习笔记
## CSS
 >#### 手机端1像素问题

```
@media (-webkit-min-device-pixel-ratio: 1.5),(min-device-pixel-ratio: 1.5)
  .border-1px
    &:after
      -webkit-transform: scaleY(0.7)
      transform: scaleY(0.7)

@media (-webkit-min-device-pixel-ratio: 2),(min-device-pixel-ratio: 2)
  .border-1px
    &:after
      -webkit-transform: scaleY(0.5)
      transform: scaleY(0.5)
```
> #### 文字过多处理

```
white-space: nowrap;
overflow: hidden;
text-overflow: ellipsis;
```
> #### 背景虚化

```
z-index: -1;
filter: blur(10px);
```
> ####  让footer固定在页面底部(sticky footer)

```
<!DOCTYPE html>
<html>

<head>
	<meta charset="UTF-8">
	<title>sticky footer</title>
	<style>
		h1 {
			text-align: center;
		}
		
		.clearfix {
			display: inline-block;
			&:after {
				content: '.';
				height: 0;
				line-height: 0;
				clear: both;
				visibility: hidden;
			}
		}
		
		.detail {
			position: fixed;
			top: 0;
			left: 0;
			z-index: 100;
			width: 100%;
			height: 100%;
			overflow: auto;
			color: #fff;
			background: rgba(7, 17, 27, 0.8);
		}
		
		.detail-wrapper {
			min-height: 100%;
		}
		
		.detail-main {
			background: rgba(7, 17, 27, 0.2);
			margin-top: 64px;
			padding-bottom: 64px;
		}
		
		.detail-close {
			position: relative;
			width: 32px;
			height: 32px;
			margin: -64px auto 0 auto;
			clear: both;
			font-size: 32px;
		}
	</style>
</head>

<body>
	<div v-show="detailShow" class="detail">
		<div class="detail-wrapper clearfix">
			<h1>Sticky footers</h1>
			<div class="detail-main">
				<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perspiciatis blanditiis aspernatur porro veniam libero earum accusamus atque facere adipisci unde officia fugiat vel tempore voluptates natus? Earum eum perferendis voluptate.</p>
			</div>
		</div>
		<div class="detail-close">
			<i class="icon-close">X</i>
		</div>
	</div>
</body>

</html>
```

***img***
	<div align="center">
		<img src="https://raw.githubusercontent.com/liuxinbin/Study-notes/master/img/stickyfooters.png" width="250" />
		<img src="https://github.com/liuxinbin/Study-notes/blob/master/img/stickyfooter01.png?raw=true" width="250" />
	</div>
	
## flex布局
1、
```
<!doctype html>
<html lang="en">

<head>
	<meta charset="UTF-8" />
	<title>flex布局</title>
	<style type="text/css">
		body {
			background: rgba(7, 17, 27, 0.8);
			color: #fff;
		}
		
		.title {
			display: flex;
			width: 80%;
			margin: 28px auto 24px auto;
		}
		
		.line {
			flex: 1;
			position: relative;
			top: -6px;
			border-bottom: 1px solid rgba(255, 255, 255, 0.2);
		}
		
		.text {
			padding: 0 12px;
			font-weight: 700;
			font-size: 14px;
		}
	</style>
</head>

<body>
	<div class="title">
		<div class="line"></div>
		<div class="text">标题</div>
		<div class="line"></div>
	</div>
</body>

</html>
```
***img***
	<div align="center">
		<img src="https://github.com/liuxinbin/Study-notes/blob/master/img/flex01.png?raw=true" width="500" />
	</div>
***





## VUE
> #### .eslintrc.js文件配置

```
 // 文件末尾强制换行
'eol-last':0,
'indent':0,
'no-tabs':'off',
// 强制在 function的左括号之前使用一致的空格
"space-before-function-paren": 0,
// 强制使用一致的反勾号、双引号或单引号,0的时候单引号和双引号都可以使用
"quotes": 0,
//if后不用空格
'keyword-spacing':0,
'comma-dangle':0
```

