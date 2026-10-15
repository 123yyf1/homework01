# 实验3 CSS 布局实战——导航菜单

## 文件说明
- `一级菜单.html`：水平排列的一级导航菜单，基于 table 布局
- `二级菜单.html`：带下拉二级菜单的导航，基于 ul/li + flex 布局

## 实现要点
1. **水平排列**：
   - 一级菜单：利用 table 天然横向排列，把 `<a>` 设为 `display:block` 做成按钮
   - 二级菜单：外层 `<ul>` 用 `display:flex` 水平排列
2. **盒模型**：通过 `padding` 控制按钮可点击区域，`border-right` 做分隔线
3. **:hover 伪类**：一级菜单悬停背景变深蓝；二级菜单项悬停文字变蓝
4. **二级下拉定位**：
   - 父 `<li>` 加 `position:relative` 作为定位上下文
   - 二级 `<ul>` 加 `position:absolute; top:100%` 钉在父项正下方，默认 `display:none`
   - 父 `<li>:hover > ul` 时 `display:block` 显示
5. **其他**：`*` 全局重置 margin/padding；`list-style:none` 去掉 ul 默认圆点；`text-decoration:none` 去掉链接下划线

## 运行方式
直接用浏览器打开两个 HTML 文件即可，无需服务器。
