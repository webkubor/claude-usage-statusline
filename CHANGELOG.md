# Changelog

## Unreleased

### Removed

- **撤掉"非仓库目录下显示子仓与分支"特性**（`73bd1ba` 撤回 `faedb6c`）。
  之前会向下找一层非 git 目录展示子仓分支，但实测在不同 shell / 配置下表现不稳，与本仓的「状态栏只反映当前工作目录」定位冲突。

## History（按 commit 时间倒序）

### 文档与品牌

- `d00ab49` — docs: 仓库改名为 claude-usage-statusline（之前的 `claude-statusline` 与 npm 上别人的包撞名）
- `118968f` — docs: 把安装细节从 README 挪到 SKILL.md，README 只保留「读懂这一行」和卖点
- `86ff44e` — docs: 显式标注为 Claude Code 工具（logo / badges / 定位语）
- `a81536a` — docs: 中英双版 README + 演示截图 + 同类对比
- `c908051` — docs: 修 clone URL 与新仓库名一致

### 特性

- `d1bed30` — feat: 主题通过文件切换，不需要重启 Claude Code
- `23eee1f` — feat(install): `--link` 模式直接 git clone 链接（不留副本），`git pull` 立即生效
- `faedb6c` — feat: 非仓库目录下显示子仓与分支 *(已撤回，见 Unreleased)*
- `7beeda1` — feat: project burn rate —— 按当前速度到不了重置时间就预警
- `c441ce1` — feat: 显示当前模型 + effort 档位；按量付费档下特别标记 200k 高价档
- `3515f99` — feat: 计费模式感知、主题化渐变条、git 状态
- `b106167` — feat: 进度条 + 本地扩展段
- `30b9c09` — fix: 显示绝对重置时间，不再用相对倒计时
- `3a46dac` — Initial commit: usage statusline for Claude Code

### 修复

- `bea9f4c` — fix: burn rate 投影限制在 5h 窗口（之前会拿整周窗口算，导致 5h 限额用户被错误预警）

---

完整 commit 列表见 `git log`。版本号随仓库 git tag 走（目前未打 tag）。