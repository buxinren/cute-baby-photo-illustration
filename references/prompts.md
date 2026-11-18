# 提示词 / Prompts

先读取照片再使用。以下基础版可直接搭配原照片；具体任务中补入实际观察到的衣服、发型、表情和道具，不编造细节。

## 中文基础版

把输入照片作为编辑对象，转换成温暖的萌宝彩铅蜡笔手绘插画。保留原人物数量、年龄感、脸型与眼形、肤色、发型、目光与表情、服装颜色和主要图案、姿势以及关键道具。面部用细腻彩铅层叠塑形，头发、衣物和物件用带纸张颗粒的蜡笔排线及粗细不均的深棕黑轮廓；脸颊添加适度的粉红斜线腮红。奶油白纸底，鲜亮而温暖的红黄蓝点色，主体周围少量爱心、星星、云朵或彩虹涂鸦，不遮脸和手。沿用原照片比例，保留关键动作。不要变成塑料3D、光滑矢量或完全写实照片；不要改变人物身份、增加人物或肢体，不要凭空添加参考图的玩偶、帽子或水果，不添加文字、署名、水印或手机界面。

## English base prompt

Edit the supplied source photograph into a warm colored-pencil and crayon baby illustration. Preserve the subject count, apparent age, face and eye shapes, skin tone, hairstyle, gaze, expression, outfit colors and main patterns, pose and important props. Use finer layered colored-pencil shading on faces, with grainy crayon hatching and irregular dark-brown or near-black outlines on hair, clothes and objects. Add moderate pink diagonal cheek hatching. Use cream paper, warm vivid red/yellow/blue accents and sparse hearts, stars, clouds or rainbow doodles around the subject, away from faces and hands. Keep the original aspect ratio and important gestures. Avoid glossy 3D, smooth vector rendering, identity replacement, extra people or limbs, and props copied from style references. Add no text, signature, watermark or phone UI.

## 多图角色声明 / Multiple inputs

“图片1是要转换的用户照片，人物与动作以图片1为准。图片2及之后仅用于笔触、纸纹、配色与涂鸦风格，不复制其中人物、道具、字幕或水印。”

“Image 1 is the edit target and identity source. Images 2 onward guide only texture, linework, palette and doodle treatment; do not copy their subjects, props, captions or signatures.”

## 常用追加指令

- 头像：使用 `avatar-clean`，做1:1头肩头像，保留完整发型，背景简洁，关键道具必要时适当拉远构图。
- 亲子：保留所有人及亲子动作，成人保持成人面部比例，儿童保持原年龄感，不把所有人婴儿化。
- 保真：降低眼睛与头部的夸张幅度，保留照片的闭眼/抿嘴/严肃表情，把风格变化集中在笔触和纸纹。
- 奶油：使用 `soft-pencil`，降低饱和度，保留温暖肤色和可见彩铅排线，不磨皮。
- 场景：保留原背景布局，把场景画成简化蜡笔背景，减少额外涂鸦。
- 海报：使用 `milestone-poster`，3:4构图，上方留白；只有我明确提供文字时才添加文字。
- 修正：以原照片保持身份与构图，只修复结果中握持道具的手指连接，其余风格、衣服与表情保持不变。

## 使用示例

上传照片后说：“使用 cute-baby-photo-illustration 的 classic-crayon，把这张照片做成手绘插画，保留原表情和衣服。”

或：“Use cute-baby-photo-illustration with avatar-clean on this photo. Keep the original expression and hairstyle.”

这些是调用示例，不是已执行或已生成的作品。
