# SKILL 资源

本目录收录可复用的 Agent Skills。每项技能独立存放，通常包含一个 `SKILL.md` 和可选的参考资料、脚本或模板。

## 目录结构

```text
SKILL/
├── README.md
└── ui-polish/
    ├── SKILL.md
    └── references/
        └── quality-rubric.md
```

`SKILL/` 是本仓库的资源目录。Codex 不会因为技能放在这里就自动加载；安装时要把某个技能目录复制到 Codex 扫描的技能路径。

## 当前技能

| 技能 | 用途 | 配套文件 |
| --- | --- | --- |
| [`ui-polish`](ui-polish/SKILL.md) | 审查并改进网站或前端界面的排版、层级、颜色、动效、交互和响应式表现。 | [`quality-rubric.md`](ui-polish/references/quality-rubric.md) |

## 安装到 Codex

### 只在当前仓库使用

在本仓库根目录执行：

```bash
mkdir -p .agents/skills
cp -R SKILL/ui-polish .agents/skills/
```

Codex 会从仓库的 `.agents/skills/` 发现技能。这样安装后，该技能随当前仓库提供。

### 在自己的所有仓库使用

在本仓库根目录执行：

```bash
mkdir -p "$HOME/.agents/skills"
cp -R SKILL/ui-polish "$HOME/.agents/skills/"
```

用户级技能适用于该用户打开的其他仓库。若目标位置已经有同名 `ui-polish` 目录，请先检查已有内容，再决定是否替换。

安装后可在 Codex 中通过 `/skills` 查看，或在任务提示中写 `$ui-polish` 显式调用。Codex 也可以根据 `SKILL.md` 前置元数据中的 `description` 判断何时使用；新安装的技能通常会自动发现，如果没有出现，重启 Codex 再检查。

其他 Agent 产品的技能发现路径可能不同。请保留整个技能子目录及其配套文件，并复制到对应产品文档指定的目录。

## 新增技能

在本目录下为每项技能新建一个独立子目录，至少包含带有 `name` 和 `description` 前置元数据的 `SKILL.md`。将技能依赖的资料放在该子目录中，并在本页的“当前技能”表格中登记。

安装前请检查技能指令和脚本，确认其来源、行为及所需权限符合预期。

## 参考

- [Codex：Build skills](https://developers.openai.com/codex/skills)
