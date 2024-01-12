# 配置说明


## 功能支持

- [] 浮动的目录样式,(sidebar-right失去焦点后自动关闭)
- [x] 添加top按钮以及快捷键 `Alt` + `g` 支持.
- [x] 代码渲染自定义(`render_codebock.html`)
- [x] 支持 pythontutor 代码可视化调试 shortcode
- [x] 支持显示`Tip`提示框 shortcode 


## 问题解决

1. sidebar-right失去焦点后自动关闭
3. 移动端滑动显示目录TOC
2. go to top 居中对齐问题


## Comment配置支持

配置 Giscus 方法:
1. 在Github创建 公开的（public）GitHub 仓库
2. 在设置中开启 Discussions 权限
3. 在项目安装 Giscus App
4. 访问 [Giscus App](https://giscus.app/zh-CN) 生成配置参数信息.
5. 将参数配置到配置文件 `params.zh.yaml` 中。


Params参数配置示例:

```yaml
services:
  giscus:
    enable: true
    repoName: "repo_name"
    repoId: ""
    category: "Announcements"
    categoryId: ""   # 通过 giscus 配置链接获取
    mapping: "pathname"
    inputPosition: "top"
    theme: "perferred_color_scheme"
    loading: "lazy"
```

## 高亮色彩方案修改

使用hugo生成高亮色彩方案CSS配置:
```bash

# 保存至 ./themes/PaperMod/assets/css/includes/chroma-styles.css 文件中

hugo gen chromastyles --style=nord > ./themes/PaperMod/assets/css/includes/chroma-styles.css

```

> 可以选择哪些色彩方案？ 访问这里[查看方案效果](https://xyproto.github.io/splash/docs/)


## 支持数学函数

- [mathjax语法参考](https://zh.wikibooks.org/wiki/LaTeX)
- [MathJax库官网](https://www.mathjax.org/)


## 字体设置

- 选择字体库: https://fonts.google.com/
- 图标字体库： https://fontawesome.com/v6/search?q=light&o=r&m=free

## ChatGPT实现代码


### TOC实现

请在这个html页面示例基础上实现浮动目录TOC效果,具体要求如下:
1. 让toc-toogle标签与 toc-siderbar放在整体的id为siderbar-right的div标签
2. 关闭toc时右侧仅仅显示toc-toogle标签在右上角。
3. 打开toc时右侧显示完整目录信息即 toc-toogle 标签，此时显示图标为关闭。
4. 标签的色彩使用nord色彩方案。

#### TOC样式自定义

- (使用中)https://codepen.io/chriscoyier/pen/bGavwRP
- 更多List样式示例: https://freefrontend.com/css-lists/


## 参考链接

- [Hugo 主题 Stack](https://stack-docs.netlify.app/zh/modify-theme/example-custom-font-family)

