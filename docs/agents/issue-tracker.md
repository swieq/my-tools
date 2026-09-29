# Issue tracker: GitHub

本仓库的任务和规格保存在 swieq/my-tools 的 GitHub Issues。
使用 gh CLI 操作；仓库身份从 git remote 推断。

## 常用操作

- 创建：gh issue create --title "..." --body-file <文件路径>
- 读取：gh issue view <编号> --comments
- 列出：gh issue list --state open --json number,title,body,labels
- 评论：gh issue comment <编号> --body-file <文件路径>
- 添加标签：gh issue edit <编号> --add-label "..."
- 移除标签：gh issue edit <编号> --remove-label "..."
- 关闭：gh issue close <编号> --comment "..."

多行正文写入临时文件，通过 --body-file 传入。

## Pull requests as a triage surface

PRs as a request surface: no.

## 技能约定

技能要求“发布到 issue tracker”时，创建 GitHub Issue。
技能要求“获取相关 ticket”时，读取对应 Issue 及评论。

GitHub 的 Issue 和 PR 共用编号空间。编号有歧义时，
先用 gh pr view <编号> 判断是否为 PR，再读取 Issue。
