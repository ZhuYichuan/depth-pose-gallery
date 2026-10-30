# Depth Pose Gallery 深度姿势参考库

深度（depth）姿势参考资产库（POSE-DB-02，原名「depthポーズ集」），来自 <https://ai-pose-depth-gallery.pages.dev/> 的本地镜像。

## 资产概览

- **总图片量**: 1439 张 PNG 原图（原寸）
- **姿势数**: 288 个姿势 × 多角度
- **分类（按系统/拍摄对象）**: 全身性感 399、全身标准 365、上半身 400、双人 275
- **角度（アングル）**: 正面 / 上から（俯视）/ 下から（仰视）/ 横 / 斜め
- **内容**: 人物姿势参考（含 depth 深度信息），分类字段（分類）如「立ち」「座り」等

## 目录结构

`分类/ID_姿势编号_角度.png`（如 `全身性感/full_sexy_P001_front.png`）

## 元数据

[`metadata_index.json`](./metadata_index.json) 每项字段：

- `id`: 图片唯一编号（如 `full_sexy_P001_front`）
- `category`: 本地中文分类目录
- `line_ja`: 原始日语系统名
- `pose_no` / `pose_name`: 姿势编号 / 姿势名称
- `angle`: 角度
- `classification`: 姿势分类（立ち / 座り 等）
- `local_path`: 本地相对路径（分类目录已由日语改中文）
- `original_url`: 原寸 PNG 地址（已下载）
- `thumb_url`: JPG 缩略图地址（未下载，可另行获取）
- `meta.total` / `meta.counts` / `meta.poses`: 总量、分类统计与姿势数

## 重新同步

```bash
curl -sL https://ai-pose-depth-gallery.pages.dev/index.json   # 完整元数据（含图片地址）
# 原寸图片地址：https://ai-pose-depth-gallery.pages.dev/img/<id>.png
# 缩略图：https://ai-pose-depth-gallery.pages.dev/thumbs/<id>.jpg
```

## 日语 → 中文 对照

| 原文 | 中文 |
|---|---|
| 全身1人・セクシー系 | 全身性感 |
| 全身1人・標準系 | 全身标准 |
| 上半身1人 | 上半身 |
| 2人絡み | 双人 |
| 系統 | 系统（分类线） |
| ポーズ | 姿势 |
| アングル | 角度 |
| 分類 | 分类（站立/坐姿等） |
| 原寸 | 原图（原尺寸） |
| サムネ | 缩略图 |
