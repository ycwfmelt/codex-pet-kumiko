# Kumiko

Codex 自定义动画宠物素材包。角色灵感来自《吹响吧！上低音号》，chibi 风格：大头窄身、棕色水手服、焦糖色蓬松侧发、蜂蜜金瞳、音符发卡，手持小号上低音号，佩戴 Codex logo 挂坠。

## 预览

Spritesheet 规格：`1536 × 1872`，8 列 × 9 行 atlas，每格 `192 × 208`。

包含动画状态：idle / running / running-right / running-left / waving / jumping / failed / waiting / review。

## 安装

将 `pet.json` 和 `spritesheet.webp` 放入 Codex 自定义宠物目录：

```bash
mkdir -p ~/.codex/pets/kumiko
cp pet.json spritesheet.webp ~/.codex/pets/kumiko/
```

或者直接克隆本仓库：

```bash
git clone https://github.com/ycwfmelt/codex-pet-kumiko.git ~/.codex/pets/kumiko
```

安装后重启 Codex，在设置中选择 **Kumiko** 即可。

## 文件说明

| 文件 | 说明 |
|------|------|
| `pet.json` | Codex 自定义宠物清单文件 |
| `spritesheet.webp` | 动画 sprite atlas（1536 × 1872，8 × 9 格） |

## 注意事项

- Codex 要求自定义宠物提供 `pet.json` + `spritesheet.webp`，atlas 中未使用的格子须为全透明。
- 已知问题：`review` 行的帧与 `running` 行重复，后续需要在 Codex 中用 `$imagegen` 重新生成并替换。
