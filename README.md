# 知识库（Knowledge Base）

本仓库只版本化可交付的知识产物，不存放编译器源码、原始语料或可重建索引。`okf/` 是唯一权威知识层；其他目录用于说明身份、证据和人工阅读入口。

## 实际目录布局

```text
kb/
├── manifest.json       # 包身份、当前发布版本及质量门
├── CHANGELOG.md        # 仓库级版本历史（只追加）
├── okf/                # OKF v0.2 知识产物，唯一权威
│   └── <domain>/
│       ├── index.md    # 领域导航
│       ├── log.md      # 领域构建明细
│       └── ...         # concept 文档
├── evidence/           # 来源清单、哈希和可追溯证据
├── human/              # handbook、FAQ 等人工阅读入口
└── .gitignore
```

`corpus/` 是外部文件系统语料的本地转换/缓存，`index/` 是可从 OKF 重建的检索索引；二者均由 `.gitignore` 排除，不进入知识库历史。Domain Package 是抽取时使用的外部构建配置，也不属于知识库交付物。

## Agent 读取顺序

1. 读 `manifest.json`：确认包身份、当前 `version` 和质量门。
2. 读 `CHANGELOG.md`：了解历次发布涉及的领域和质量状态。
3. 进入 `okf/<domain>/index.md`：浏览领域知识；需要构建细节时读同目录 `log.md`。
4. 需要核验来源时读 `evidence/<domain>/`；面向人的概览从 `human/` 开始。

## 版本与发布

- `main` 始终表示最新已发布、通过质量门的知识库状态。
- 每次发布提交都创建一个 annotated Git tag，格式为 `vYYYY.MM.DD`；同一天再次发布依次使用 `.2`、`.3`。
- tag 与发布提交一一对应且禁止覆盖。检出 tag 可得到当时完整、可复现的知识库快照。
- `manifest.json.version` 必须与当前提交的发布 tag 一致。
- `CHANGELOG.md` 保存仓库级历史，`okf/<domain>/log.md` 保存领域级明细。
- 使用 `--push` 发布时，`main` 与本次 tag 一并推送到远端。

## Git 边界

允许提交的顶层路径仅为 `manifest.json`、`CHANGELOG.md`、`README.md`、`.gitignore`、`okf/`、`evidence/` 和 `human/`。发布器在提交前会检查暂存区；若混入源码或其他非知识产物，将拒绝提交。
