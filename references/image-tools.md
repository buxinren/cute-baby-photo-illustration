# 图像编辑能力衔接 / Image-tool integration

## 能力边界

| 宿主能力 | 本 Skill 的行为 | 实际交付 |
|---|---|---|
| 可读取图片且可调用图片编辑工具 | 查看原图，构造提示词，附原图调用编辑，检查结果 | 工具生成的真实图片 |
| 只能看图或输出文字 | 提取保留项，说明不能出图，提供提示词 | 文本，不是转换成品 |
| 图片附件无法读取 | 请求重新上传或提供宿主能读取的路径 | 不凭空描述照片 |

This repository is an instruction package. It ships no model weights, executable image client, server, API key or paid service integration. Installing it does not add image editing to a text-only agent. The agent can use an existing compatible image-editing tool; tool availability, costs and permissions are controlled by the host.

## 有内置图像编辑工具时

1. 读取当前工具的真实说明与参数；不要假设所有宿主都使用相同名称或参数。
2. 将原照片作为编辑目标，将另附插画明确标记为风格参考。保留项应来自原照片，而不是风格图。
3. 对支持本地路径的工具，先查看本地照片，再传入路径。对只接受对话附件的工具，使用可访问的附件；不能访问时请求重传。
4. 传入完整编辑指令，并按工具支持设置实际宽高比、尺寸或透明背景。普通纸底图不需要透明背景。用户要透明贴纸时去掉纸底并请求真正的透明通道。
5. 等待工具真实返回，检查图片。调用失败即报告失败，不能把生成中的任务或提示词当作成品。

## Codex 内置 image_gen 的条件示例

仅当当前宿主实际暴露相应工具时适用。工具的最新说明优先于本文件。

- 本地文件先通过图片查看能力检查；若工具支持 `referenced_image_paths`，传入实际目标与参考路径。
- 仅有对话图片且工具支持 `num_last_images_to_include` 时，使用包含所有目标的最小图片数量。
- 不同时提供这两种输入方式。任何目标无法纳入时，请用户重新附图。
- 用 `prompt` 明确图片角色与保留项；按请求设置 `transparent_background`。
- 不为内置工具索要 API 密钥。没有内置能力时，不擅自改走付费 API；用户选择外部服务后再按其官方文档配置。

## Prompt-only fallback

Say: “当前环境没有可调用的图像编辑工具。以下是可用于支持图片编辑的工具的提示词，尚未生成图片。” Then return a completed prompt with observed preservation details, chosen preset, composition and constraints. If the source image itself is unavailable, label the prompt generic rather than claiming visual analysis.
