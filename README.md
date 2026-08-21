# 随想记录员

专用 Hermes Agent：把口语化所思所想整理后，按天写入本地 Markdown。不是通用助手。

## 安装

需要 Hermes `>= 0.20.0`。

```bash
hermes profile install github.com/lessore/thought-recorder --alias
```

然后做两件事，否则会写错地方或没有模型：

1. 改记录目录。打开 `~/.hermes/profiles/thought-recorder/AGENTS.md`，把里面的绝对路径改成这台机器上你要存笔记的目录。
2. 配模型和密钥：

```bash
thought-recorder setup
```

建议把工作目录指到 profile 自己，这样每次都会加载 `AGENTS.md`：

```bash
thought-recorder config set terminal.cwd "$HOME/.hermes/profiles/thought-recorder"
```

启动：

```bash
thought-recorder chat
```

更新（记忆和 `.env` 会保留）：

```bash
hermes profile update thought-recorder
```

## 这台机器上的作者目录

活的 profile 在 `~/.hermes/profiles/thought-recorder`。流程以 `AGENTS.md` 为准，`SOUL.md` 是身份。
