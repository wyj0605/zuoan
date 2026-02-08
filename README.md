# 左岸书（Zuo An Shu）

本仓库提供《左岸读书·微志》的 EPUB 电子书，用于离线阅读与留存。

## 背景与来源
- 抓取时间：2015 年 12 月
- 来源网站：zreading.com（目前已无法访问）
- 说明：当年从网站抓取并整理为电子书，现以备份形式保存，供朋友们下载阅读。

## 文件说明
- 电子书文件：`Zuo An Du Shu - Wei Zhi.epub`、`Zuo An Du Shu - Wei Zhi.mobi`
- 格式：EPUB、MOBI（通用电子书格式，适配多平台与设备）
 - 原始数据文件：`zuoan.sql`（用于再制作与数据恢复）

## 如何阅读
- macOS / iOS：使用 `Apple Books` 或 `Calibre`
- Windows / Linux：使用 `Calibre`
- Android：使用 `ReadEra`、`PocketBook` 等支持 EPUB 的阅读器
- Kindle 设备：使用 MOBI 文件；或通过“发送至 Kindle”支持 EPUB
- 其他：任何支持 EPUB 的阅读器皆可直接打开

## 下载方式
- 直接下载本仓库中的 `Zuo An Du Shu - Wei Zhi.epub` 或 `Zuo An Du Shu - Wei Zhi.mobi` 文件即可。

## 再制作（技术向）
- 提供 `zuoan.sql` 原始数据，供具备技术能力的朋友重新制作电子书。
- 恢复数据：将 `zuoan.sql` 导入本地数据库（如 MySQL），根据表结构导出文章内容与元数据。
- 生成文稿：按时间或栏目整理为单一 `Markdown` 或 `HTML` 文件。
- 生成 EPUB（任选其一）：
  - Pandoc：`pandoc input.md -o zuoan.epub --metadata title=\"左岸读书·微志\" --toc`
  - Calibre：`ebook-convert input.html zuoan.epub --language zh --title \"左岸读书·微志\" --embed-all-fonts`
- 工具建议：`Pandoc`、`Calibre`、或自定义脚本（Python/Node）批量生成目录与样式。
- 欢迎改进制作流程或样式并反馈。

## 致谢与声明
- 内容版权归原作者及左岸读书网站所有。
- 本项目仅用于非商业的备份与学习交流。
- 如权利人认为不宜公开，请联系我处理。

## 维护
- 不定期维护。如发现排版或内容问题，欢迎反馈与指正。