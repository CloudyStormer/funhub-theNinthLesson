# 今晚连产测试状态

## 自动化

名称：今晚AI漫剧连产测试  
频率：约每30分钟运行一轮  
目标：每轮推进一集或补齐当前集的 review 包。

## Review 目录

所有可检查文件统一放这里：

```text
C:/Users/Administrator/Documents/Codex/2026-05-21/img2-0-codex/ai_manjv_campus_horror/review
```

## 当前进度

| 集数 | 状态 | Review |
| --- | --- | --- |
| 第1集 | 已整理 review 入口 | `review/episode01_review.html` |
| 第2集 | 本轮已生成文字预览包 | `review/episode02_review.html` |
| 第3集 | 待下一轮继续 | 待生成 |

## 自动化每轮必须输出

1. 做了哪一集。
2. 生成/修改了哪些文件。
3. Review HTML 的绝对路径。
4. 下一轮继续哪一集。

## 说明

当前本机没有检测到 `ffmpeg`，所以今晚先用 HTML 预览页作为 review 位置。HTML 预览页相当于“视频粗剪板”：包含镜头顺序、画面参考、字幕、声音和图生视频提示词。等接入视频生成/剪辑工具后，再输出真正 MP4。

