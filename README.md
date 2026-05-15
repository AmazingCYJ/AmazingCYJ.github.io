# AmazingCYJ Blog

Hexo + Butterfly personal blog for AmazingCYJ.

## Development

```bash
npm install
npm run server
```

Create a new post:

```bash
npm run new -- "文章标题"
```

Post files are generated under `source/_posts/`.

## Build

```bash
npm run build
```

## Comments

评论系统使用 Butterfly 内置的 Disqus 集成，效果和参考站一致。

当前项目配置：

```yaml
comments:
  use:
    - Disqus

disqus:
  shortname: amazingcyj
```

Disqus 后台需要这样配置：

1. 在 Disqus 创建站点：https://disqus.com/admin/create/
2. Website Name 可以填 `AmazingCYJ`
3. Website URL 填 `https://amazingcyj.github.io`
4. Shortname 尽量填 `amazingcyj`
5. 如果 Disqus 分配了别的 shortname，修改 `_config.butterfly.yml` 里的 `disqus.shortname`
6. 在 Disqus 后台 `Settings -> Reactions` 打开表情反应，才会出现参考站那种 Upvote / Funny / Love 等按钮

修改配置后本地预览：

```bash
npm run preview
```

访问文章详情页底部，例如：

```text
http://localhost:4000/study/hello-agent-era/#post-comment
```

注意：首页、分类页、关于页不会显示评论框，只有文章详情页底部会显示。
