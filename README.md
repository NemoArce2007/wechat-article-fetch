# wechat-article-fetch

抓取微信公众号文章，转成 Markdown，并洗掉广告和格式问题。

给一个 `mp.weixin.qq.com` 链接即可。脚本把正文和图片落到指定目录，Agent 再按技能说明删关注引导、课程推广和多余空行。

## 安装

```bash
npx skills add NemoArce2007/wechat-article-fetch -g -y
```

手动安装时，把 `skills/wechat-article-fetch/` 整目录复制到下表的用户目录。Cursor 云端只认 `~/.cursor/skills/` 里的真实文件，不要用符号链接。

| Agent | 全局目录 |
| --- | --- |
| Cursor（含云端同步） | `~/.cursor/skills/wechat-article-fetch/` |
| Claude Code | `~/.claude/skills/wechat-article-fetch/` |
| Codex | `~/.codex/skills/wechat-article-fetch/` |
| 其他按 Agent Skills 读取的客户端 | `~/.agents/skills/wechat-article-fetch/` |

Cursor 云端：设置 → Agents → Context and Tools，打开 **Sync Skills for Cloud Agents**。同步的是你自己的私有副本，和这个公开仓库是两回事。

## 用法

依赖：

```bash
pip install -r requirements.txt
```

```bash
python skills/wechat-article-fetch/wechat_article_to_md.py <文章URL> <输出目录>
python skills/wechat-article-fetch/wechat_article_to_md.py <文章URL> <输出目录> --no-images
```

视频下不了，只留位置标记。文章有访问限制时脚本会报错。

## 许可

[MIT](LICENSE)
