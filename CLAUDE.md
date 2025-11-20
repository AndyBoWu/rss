# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

这是一个中文RSS订阅源精选项目，收集和整理高质量的中文RSS订阅源，涵盖科技、AI、网络小说、旅游等主题。项目以OPML格式组织订阅源，方便用户导入到Reeder等RSS阅读器。

## Project Structure

```
.
├── README.md                   # 项目说明文档（中文）
├── CLAUDE.md                   # Claude Code工作指南
└── chinese-rss-feeds.opml     # 主要的OPML订阅源文件
```

## File Formats

### OPML Format
- 项目使用OPML 2.0格式组织RSS订阅源
- OPML是基于XML的格式，用于RSS阅读器导入/导出订阅列表
- 每个订阅源包含：`text`（显示名称）、`xmlUrl`（RSS地址）、`htmlUrl`（网站地址）

## Content Categories

项目按以下四个主题分类组织RSS源：

1. **科技** - 个人技术博客、技术媒体、技术团队博客、开发者社区
2. **AI 人工智能** - AI相关博客和新闻源
3. **网络小说** - 起点中文网、晋江文学城（通过RSSHub）
4. **旅游** - 旅游媒体和博客

## Adding New RSS Sources

添加新RSS源时，请遵循以下步骤：

1. **验证RSS源质量**：
   - 更新频率稳定（至少每月更新）
   - 内容原创性高或有独特价值
   - 中文内容为主

2. **确定分类**：
   - 将RSS源添加到正确的分类下
   - 如果是技术类，进一步细分到子分类（个人博客/技术媒体/技术团队等）

3. **OPML格式**：
   ```xml
   <outline type="rss"
            text="显示名称"
            title="显示名称"
            xmlUrl="https://example.com/feed.xml"
            htmlUrl="https://example.com/"/>
   ```

4. **使用RSSHub**：
   - 对于不提供RSS的网站，使用RSSHub生成RSS源
   - 格式：`https://rsshub.app/{route}`
   - 参考：https://docs.rsshub.app/

5. **更新README.md**：
   - 在对应分类中添加新源的说明
   - 保持README与OPML文件同步

## Quality Standards

- ✅ 更新频率稳定
- ✅ 内容原创性高
- ✅ 专业深度或实用价值
- ✅ 中文内容为主

## RSSHub Usage

部分订阅源通过RSSHub生成：

- **起点中文网**：
  - 作者作品：`/qidian/author/{作者ID}`
  - 小说讨论区：`/qidian/forum/{小说ID}`
  - 限时免费：`/qidian/free`

- **晋江文学城**：
  - 作品更新：`/jjwxc/book/{作品ID}`
  - 作者作品：`/jjwxc/author/{作者ID}`

## Maintenance Tasks

定期维护任务：

1. **验证RSS源可用性**：
   - 检查RSS链接是否仍然有效
   - 移除长期无响应的源

2. **更新RSSHub路由**：
   - RSSHub路由可能因网站更新而变化
   - 参考最新文档更新路由地址

3. **添加新源**：
   - 关注社区推荐的优质RSS源
   - 保持列表的时效性和相关性

## Development Workflow

这是一个内容管理项目，不涉及代码开发：

- 直接编辑 `chinese-rss-feeds.opml` 添加/修改RSS源
- 同步更新 `README.md` 中的内容分类说明
- 提交时使用清晰的commit message，说明添加/删除了哪些RSS源

## Import URL

用户可以通过以下GitHub raw URL直接导入OPML文件（支持Inoreader、Feedly等阅读器）：

```
https://raw.githubusercontent.com/andybowu/rss/main/chinese-rss-feeds.opml
```

**注意**：修改OPML文件后，用户需要重新导入URL才能获取最新内容。

## Resources

- [OPML Specification](http://opml.org/spec2.opml)
- [RSSHub Documentation](https://docs.rsshub.app/)
- [Gracker/Rss-IT](https://github.com/Gracker/Rss-IT) - 科技博客收集
- [top-rss-list](https://github.com/weekend-project-space/top-rss-list) - 热门中文RSS源
