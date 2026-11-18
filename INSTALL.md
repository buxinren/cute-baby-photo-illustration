# 安装 / Installation

## 准备

下载仓库 ZIP 并解压，将最外层项目目录整理为 `cute-baby-photo-illustration`。保留 `SKILL.md` 和 `references` 的相对位置；单独复制 `SKILL.md` 会丢失预设与提示词。

宿主必须支持 Agent Skills 或能读取这些指令；实际出图还需要可用的图片编辑工具。不要把“安装成功”理解为“图片服务已开通”。

## Codex 本地安装

按当前官方文档，用户级目录为 `~/.agents/skills`，项目级可放在项目的 `.agents/skills`。下方采用用户级目录；部分已有安装可能使用 `~/.codex/skills` 或自定义目录，应以实际宿主配置为准。不要同时放置多个同名版本。

Windows PowerShell，先进入解压后的项目目录，再执行：

```powershell
$skillRoot = Join-Path $env:USERPROFILE '.agents/skills'
$skillTarget = Join-Path $skillRoot 'cute-baby-photo-illustration'
if (Test-Path -LiteralPath $skillTarget) { throw '同名 Skill 已存在，请先备份并决定如何更新。' }
New-Item -ItemType Directory -Force -Path $skillRoot | Out-Null
Copy-Item -LiteralPath (Get-Location).Path -Destination $skillTarget -Recurse
```

macOS/Linux，在解压后的项目目录执行：

```sh
skill_root="$HOME/.agents/skills"
skill_target="$skill_root/cute-baby-photo-illustration"
if [ -e "$skill_target" ]; then
  echo 'Skill already exists; back it up before updating.'
else
  mkdir -p "$skill_root"
  cp -R . "$skill_target"
fi
```

安装后应存在 `cute-baby-photo-illustration/SKILL.md`，其同级为 `references/`。重新打开会话或刷新宿主技能列表，然后上传照片并明确说“使用 cute-baby-photo-illustration”。宿主界面与发现路径可能随版本不同，参阅 [官方技能文档](https://learn.chatgpt.com/docs/build-skills)。

## Other hosts / 无需安装

For another Agent Skills host, copy the complete folder to its documented skill directory. The package does not assume identical discovery paths or tool names across products. If the host cannot install skills, attach `SKILL.md` and the relevant `references/` files as instructions for a single conversation.

Installing instructions alone does not provide image editing. Attach the original photo and verify the host offers an image-input editing tool.

## 排查 / Troubleshooting

- 找不到 Skill：检查是否多嵌套了一层目录，是否存在重复同名版本，实际技能目录是否正确，并刷新会话。
- 只输出文字：检查是否只有看图/文本能力；要求助手明确说明是否调用了图片编辑工具。
- 图片无法读取：重新上传照片；另一个会话中的图片不一定自动可用。
- 身份或衣服漂移：要求使用原照片为编辑目标，降低夸张程度；只参考风格图的线条与配色。
- 不要在聊天或仓库中粘贴服务密钥。本包不需要密钥；另选外部服务时按该服务的说明单独配置。

更新前备份旧目录，避免覆盖本地改动。卸载时移除安装的这一份技能目录即可；不要误删存放在别处的照片或成品。
