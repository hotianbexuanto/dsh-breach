# 更新日志

> 这个文件就是更新弹窗里显示的「更新内容」。
> 想改文案，直接改这里；后端每次检查更新都会重新读它，不用动代码。

## 1.3.1

### 修复

- **点「重启」后 DSH 崩溃**：`shell.overlay` 槽位抛 React error #31（渲染了 `{kind, text}` 对象），宿主判定 entry crashed 后直接 fatal 退出。
- **asar 被占用时强杀 DSH**：旧逻辑等 10 秒改不动名就杀掉所有 DSH 进程，用户看到「host stopped」弹窗。现改为继续轮询并提示用户手动退出。

### 新增

- **更新确认弹窗**：更新胶囊不再点一下就更新，改为弹窗展示本文件内容，可选「立即更新」或「稍后」。

### 优化

- locale / command 返回值统一收敛为字符串（`safeText`），杜绝对象进 React children。
- 5 个 overlay 组件各自包一层错误边界（`SlotSafe`），单个组件异常只降级自己。

## 1.3.0

- 适配 DSH 0.2.2-rc.1，8 条断锚补变体。
- 修复 asar 挪不走导致补丁白打：改为反复重试改名。
- 新增 `ptc-executor` / `dsh-tools-pipeline` / `deliverable-file-refs` 路径键。

## 1.2.9

- 回退 UI 改进：只隐藏被撤掉的那一轮。
- 设置面板增加 hooks 拒绝开关。
