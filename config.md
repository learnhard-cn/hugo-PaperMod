# 配置说明


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
