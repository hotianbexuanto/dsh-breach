Give DeepSeek Harness a foundation that will actually work: inject the identity, disclaimer, and approval sections of the system prompt, rewrite the rules, and lay a revertible host patch engine over the checkout. Prompts are per-model, and the default one targets the Chinese model 小码酱.

The panel lives at Settings → Plugins → dsh-breach: attach a prompt per model, try them one at a time, roll back in one click when a change breaks something.

### Install

**DSH → Plugins → Add plugin → paste:**

```
https://github.com/zhuchongba-01/dsh-breach
```

> npm carries only an empty `0.0.0-stage` shell, so the bare package name answers "this package declares no bundle".

**It rewrites host source.** Every change leaves a `.dshhappy.bak` backup and reverts in one click, but no host version is guaranteed compatible and a host upgrade may leave the revert incomplete — back up first.

![dsh-breach panel](./docs/overview.png)
