# 风格预设 / Style presets

这些是审美指令，不是模型参数或训练权重。默认强度中等；用户要求保真时减小头眼夸张，不减弱纸张与笔触质感。

| ID | 适用 | 具体处理 |
|---|---|---|
| `classic-crayon` | 默认、与参考方向最接近 | 细腻彩铅面部，粗糙深色轮廓，红黄蓝点色，奶油纸底，斜线腮红，少量涂鸦 |
| `soft-pencil` | 温柔、奶油色版本 | 更细的棕色线，浅桃粉/黄/蓝，轻交叉排线，保留纸纹，减少背景装饰 |
| `playful-doodle` | 活泼、童趣版本 | 更明显蜡笔颗粒和随手线条，鲜亮原色，小星星与动态短线；不自动改变表情 |
| `avatar-clean` | 头像 | 1:1，头肩构图，保持发型完整，人物居中，背景只留一到两个装饰；不硬裁手中关键道具 |
| `milestone-poster` | 成长纪念海报 | 默认3:4，保留主体姿势，适当留白；只有用户提供文字时才排入文字，未提供时不编造姓名/生日 |

## Common invariants (English)

Preserve identity cues, apparent age, skin tone, expression, clothing, pose, subject count and important props. Render faces with finer colored-pencil shading and outer edges with uneven crayon strokes. Keep visible paper grain. Decorative doodles must stay away from faces and hands. Style references do not supply a replacement identity or mandatory props.

## 参考图观察

第一张参考的面部更细腻，红帽与条纹衣物使用更重的蜡笔颗粒；第二张把坐姿、座椅及周围物件组织成完整构图，外轮廓与彩虹更粗糙；第三张是多幅不同姿势、表情、衣服的拼图，共同点是斜线腮红、鲜亮色块和深色手绘轮廓。上述仅记录视觉特征，不复制原图、作者水印或参考角色。
