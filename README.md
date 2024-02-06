# 设置顶栏为透明,以及修改 dash 的圆润度和透明度

## 1.安装优化

```bash
$ sudo apt-get install gnome-tweak-tool
```

## 2.安装拓展管理器

```bash
$ sudo apt-get install extension-manager
```

## 3.进入优化中,选择一个 shell 主题

## 4.编辑 css 文件

```bash
$ cd /usr/share/gnome-shell/theme/主题名字
$ vim ./gnome-shell.css
```

## 修改顶栏透明度:修改`background-color`

```css
/* Top Bar */
#panel {
	background-color: rgba(0, 0, 0, 0);
	font-weight: bold;
	height: 2.2em;
	transition-duration: 250ms;
	box-shadow: inset 0 -1px 0 0 #0e0e0e;
}
```

```css
#dashtodockContainer.bottom.shrink #dash .dash-background {
	margin: 0;
	margin-bottom: 4px;
	padding: 2px;
	border-radius: 18px;
	spacing: 5px;
}
```

## 修改 dash 圆润度:修改`border-radius`

```css
.dash-background {
	background-color: #373737;
	border-radius: 18px;
	padding: 12px;
	spacing: 6px;
	margin-bottom: 12px;
	border: 1px solid #464646;
}
```

## 修改 dash 透明度:搜索:`.dash-background`

```css
#dashtodockContainer.bottom #dash .dash-background,
#dashtodockContainer.bottom.dashtodock #dash .dash-background,
#dashtodockContainer.bottom.shrink #dash .dash-background {
	background: rgba(19, 19, 19, 0.35);
	transition-duration: 250ms;
}
```
