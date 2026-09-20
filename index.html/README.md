# 用户注册页面（实验2 HTML5进阶综合训练）

## 作业内容

本项目综合运用 HTML5 的列表、表格、表单三大模块知识，制作了一个完整的"用户注册"页面，并通过 JavaScript 监听表单提交事件，在浏览器 Console 面板打印收集到的表单数据。

## 文件结构

| 文件 | 说明 |
| --- | --- |
| index.html / register.html | 用户注册主页面（两个文件内容一致，index.html 为主文件） |
| style.css | 页面样式表 |
| register.js | 表单提交事件监听与数据收集脚本 |
| README.md | 作业说明文档 |

## 使用到的标签

### 语义化结构标签
- `<header>`：页面头部，包含主标题 `<h1>` 和导航 `<nav>`
- `<main>`：表单主体区域
- `<footer>`：页面底部版权信息
- `<section>`：内容分区

### 列表标签
- `<ul>`：无序列表，制作站点导航和"注册流程"
- `<ol>`：有序列表，制作"注册步骤"说明
- `<dl>` / `<dt>` / `<dd>`：定义列表，制作"常见问题"板块

### 表格标签
- `<table>` / `<tr>` / `<th>` / `<td>`：搭建"会员权益对比"表格
- `<thead>` / `<tbody>`：划分表格区域
- `rowspan` / `colspan`：实现单元格合并

### 表单标签
- `<form>`：定义表单，设置 `action="register.php"`、`method="post"`
- `<input>`：多种类型（text、password、radio、checkbox、file、email、tel、date）
- `<select>` / `<option>`：所在城市下拉选择，默认选中"长沙"
- `<textarea>`：个人简介多行文本
- `<button>`：提交按钮与重置按钮
- `<label>`：使用 `for + id` 与包裹式两种关联方式

### 表单核心属性
- `name`：数据提交的字段名
- `placeholder`：占位提示
- `required`：必填校验
- `pattern`：手机号正则校验（`[0-9]{11}`）
- `checked`：单选框默认选中
- `selected`：下拉框默认选中
- `accept` / `multiple`：头像文件上传限制与多选

## 遇到的困难及解决方法

1. **确认密码与密码一致性校验**：最初只做了前端展示，没有校验逻辑。
2. **同名复选框数据收集**：`FormData` 遍历同名控件时值会互相覆盖。解决方法：判断字段名是否已存在，存在则转为数组存储，保证多个兴趣选项都能被收集到。
3. **标签与控件关联**：初期所有控件用包裹式 `<label>`，无法覆盖全部场景。解决方法：研究 `<label>` 的两种用法（`for + id` 与包裹式），在性别单选组中两种方式各使用一次。
4. **页面布局混乱**：标签、控件堆叠在一起。解决方法：使用 CSS 统一控制表单控件宽度、间距与对齐，并用 `<fieldset>` 对表单分区。

## 运行方式

1. 使用 Visual Studio Code 打开本项目目录
2. 安装并启用 Live Server 插件，右键 `index.html` 选择 "Open with Live Server"
3. 按 F12 打开 Chrome DevTools，填写表单并点击"注册"，在 Console 面板查看收集到的数据