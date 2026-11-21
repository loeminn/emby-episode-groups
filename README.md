# Emby 剧集组

用于 Emby 神医助手的本地剧集组 JSON 配置。

## 物语系列 · TV（首播日期）

- TMDB ID `46195`
- [下载 episodegroup.json](https://raw.githubusercontent.com/loeminn/emby-episode-groups/main/46195/episodegroup.json)
- [查看配置](46195/episodegroup.json)
- 以 TMDB 剧集组为基础，S07 的「扇·公式」按 BD 分为两话，共 12 组、122 集。季标题参考下表所列 Bangumi 条目的中文名。[TMDB 参考剧集组](https://www.themoviedb.org/tv/46195/episode_group/6a125fe96d1fa649f9d49475?language=zh-CN)

将 `episodegroup.json` 放入《物语系列》的节目根目录，在神医助手中开启“启用本地剧集组 TMDB”，并将视频或 STRM 文件按下表的本地季集编号入库。[神医助手使用说明](https://github.com/sjtuross/StrmAssistant/wiki/本地剧集组刮削)

| 季标题 | 本地编号 | Bangumi 条目 |
| --- | --- | --- |
| Specials | S00E01–S00E05 | — |
| 化物语 | S01E01–S01E15 | [1671](https://bgm.tv/subject/1671) |
| 伪物语 | S02E01–S02E11 | [23161](https://bgm.tv/subject/23161) |
| 猫物语（黑） | S03E01–S03E04 | [56117](https://bgm.tv/subject/56117) |
| 物语系列 第二季 | S04E01–S04E26 | [68812](https://bgm.tv/subject/68812) |
| 花物语 | S05E01–S05E05 | [82322](https://bgm.tv/subject/82322) |
| 凭物语 | S06E01–S06E04 | [115932](https://bgm.tv/subject/115932) |
| 终物语 | S07E01–S07E13 | [138829](https://bgm.tv/subject/138829) |
| 历物语 | S08E01–S08E12 | [146104](https://bgm.tv/subject/146104) |
| 终物语（下） | S09E01–S09E07 | [175596](https://bgm.tv/subject/175596) |
| 续·终物语 | S10E01–S10E06 | [233926](https://bgm.tv/subject/233926) |
| 物语系列 外传季&怪物季 | S11E01–S11E14 | [475354](https://bgm.tv/subject/475354) |

### S07 终物语的 BD 分集

| 本地编号 | 内容 | TMDB 原始编号 |
| --- | --- | --- |
| S07E01 | 扇·公式 其一 | S04E01 |
| S07E02 | 扇·公式 其二 | S04E01 |
| S07E03–S07E13 | 育·谜题 其一至忍·盔甲 其六 | S04E02–S04E12 |

前两话需要分别使用 BD 分集文件入库。TMDB 将两话合为一条，前两集会共用该条目的元数据。[Bangumi 分集](https://bgm.tv/subject/138829/ep) · [BD 收录信息](https://www.monogatari-series.com/owarimonogatari/package/01.html) · [TMDB 合集条目](https://www.themoviedb.org/tv/46195/season/4/episode/1?language=zh-CN)

剧集组 JSON 的 `name` 用于季标题。要在 Emby 中分别显示这两集的 Bangumi 标题，请启用媒体库的 NFO 元数据读取器，将下面的文件放到对应 BD 视频或 STRM 文件旁边，并确保除扩展名外文件名完全相同。放好后扫描媒体库。如已有同名 NFO，可在现有文件里更新 `<title>`，并将 `Name` 加入 `<lockedfields>`。[Emby NFO 说明](https://emby.media/learn/articles/metadata-discovery/local-formats/Metadata-NFO.html)

- `S07E01` 扇·公式 其一。[下载 NFO](https://raw.githubusercontent.com/loeminn/emby-episode-groups/main/46195/nfo/S07E01.nfo)
- `S07E02` 扇·公式 其二。[下载 NFO](https://raw.githubusercontent.com/loeminn/emby-episode-groups/main/46195/nfo/S07E02.nfo)

已经入库时，也可以在两集的「编辑元数据」里分别修改标题并锁定「名称」字段。[Emby 元数据管理说明](https://emby.media/support/articles/Metadata-manager.html)

## 哈哈哈哈哈 · 第 6 季

- TMDB ID：`112732`
- [下载 episodegroup.json](https://raw.githubusercontent.com/loeminn/emby-episode-groups/main/112732/season-06/episodegroup.json)
- [查看配置](112732/season-06/episodegroup.json)
- 排列：每期 **正片上 → 正片下 → 加更**，共 12 期、36 集。
- 本地季号保持 **第 6 季**，本地集号为 **S06E01–S06E36**。
- 核对日期：2026-10-06。

### 使用方法

1. 下载配置，文件名保持为 `episodegroup.json`。
2. 将文件放入《哈哈哈哈哈》的**节目根目录**，与 `Season 06` 目录同级。
3. 启用神医助手的“启用本地剧集组 TMDB”，并确认节目 TMDB ID 为 `112732`。
4. 按下表为视频或 STRM 文件设置本地季集编号，再入库或刷新元数据。

本配置只定义第 6 季。若节目根目录已有其他季的 `episodegroup.json`，请将本文件中 `order: 6` 的分组合并到原文件的 `groups` 数组（已有第 6 季分组则替换该组）。

JSON 中分组 `order: 6` 表示本地第 6 季；集的 `order` 从 0 开始，对应本地集号减 1。`season_number` 和 `episode_number` 指向 TMDB 原始条目。

修改配置后若未生效，可重启 Emby 清除神医助手的剧集组缓存，再刷新元数据。仓库中的配置不会自动同步到媒体目录。

### 收录范围

保留 TMDB 第 6 季已明确标注的正片第 1–24 集原始顺序，并将特别篇第 65–76 集的“第6季 第N期加更”插入各期下集之后。

核对时 TMDB 第 6 季还列有第 25–36 集，但这些条目仅显示默认集名，无播出日期及有效简介，无法确认内容，因此未纳入，也未将其猜测为加更。

### 季集映射

| 本地编号 | 内容 | TMDB 原始编号 |
| --- | --- | --- |
| S06E01 | 第1期上 | S06E01 |
| S06E02 | 第1期下 | S06E02 |
| S06E03 | 第1期加更 | S00E65 |
| S06E04 | 第2期上 | S06E03 |
| S06E05 | 第2期下 | S06E04 |
| S06E06 | 第2期加更 | S00E66 |
| S06E07 | 第3期上 | S06E05 |
| S06E08 | 第3期下 | S06E06 |
| S06E09 | 第3期加更 | S00E67 |
| S06E10 | 第4期上 | S06E07 |
| S06E11 | 第4期下 | S06E08 |
| S06E12 | 第4期加更 | S00E68 |
| S06E13 | 第5期上 | S06E09 |
| S06E14 | 第5期下 | S06E10 |
| S06E15 | 第5期加更 | S00E69 |
| S06E16 | 第6期上 | S06E11 |
| S06E17 | 第6期下 | S06E12 |
| S06E18 | 第6期加更 | S00E70 |
| S06E19 | 第7期上 | S06E13 |
| S06E20 | 第7期下 | S06E14 |
| S06E21 | 第7期加更 | S00E71 |
| S06E22 | 第8期上 | S06E15 |
| S06E23 | 第8期下 | S06E16 |
| S06E24 | 第8期加更 | S00E72 |
| S06E25 | 第9期上 | S06E17 |
| S06E26 | 第9期下 | S06E18 |
| S06E27 | 第9期加更 | S00E73 |
| S06E28 | 第10期上 | S06E19 |
| S06E29 | 第10期下 | S06E20 |
| S06E30 | 第10期加更 | S00E74 |
| S06E31 | 第11期上 | S06E21 |
| S06E32 | 第11期下 | S06E22 |
| S06E33 | 第11期加更 | S00E75 |
| S06E34 | 第12期上 | S06E23 |
| S06E35 | 第12期下 | S06E24 |
| S06E36 | 第12期加更 | S00E76 |

### 参考

- [TMDB 第 6 季](https://www.themoviedb.org/tv/112732/season/6?language=zh-CN)
- [TMDB 特别篇](https://www.themoviedb.org/tv/112732/season/0?language=zh-CN)
- [神医助手：本地剧集组刮削](https://github.com/sjtuross/StrmAssistant/wiki/本地剧集组刮削)

本仓库仅提供季集映射配置，不包含视频或播放资源。

