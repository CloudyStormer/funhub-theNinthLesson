# 场景生成记录 A

本批次使用内置 `image_gen` 模式生成／编辑，最终图片均为横版 16:9（1672 × 941），用于平台“新建集”阶段的全局空间锚点。所有成品均已按原图进行视觉质检：无人物、无可读文字、无 Logo、无水印。

## 1. 普通教室_空景.png

- 模式：`precise-object-edit`
- 原始参考图：`第二版/第01集_我说我夜盲/clip首尾帧图/clip01_白天教室宣布晚自习/clip01_首帧.png`
- 最终编辑目标：第一轮去除人物后得到的空教室草稿（该草稿只保留在 Codex 生成缓存中）
- 最终提示词：

```text
Use case: precise-object-edit
Asset type: episode-global empty-location reference anchor for AI comic-video production
Input image 1: edit target.
Primary request: Keep this same empty daytime classroom, but correct only the layout for a production-ready spatial anchor.
Furniture correction: show exactly 25 complete single-person desk-and-chair sets in a clean 5-by-5 grid: five columns across and five rows deep. All 25 desktop surfaces and all 25 matching chairs must be present, aligned, and fully inside the frame; no cropped partial desks at either edge; maintain a clear center aisle.
Door correction: widen the rear-wall viewpoint just enough that BOTH classroom doors on the RIGHT wall are visible—the front door near the blackboard and the rear door nearer the camera. The entire window row remains along the LEFT wall. Camera is at the rear center looking toward blackboard and lectern.
Constraints: keep the classroom completely empty. Preserve the same cool-white daytime window light, semi-realistic Chinese-animation style, blackboard, wooden lectern, gray-blue wall treatment, tiled floor and 16:9 wide establishing-shot look.
Avoid: any person, teacher, student, head, hand, body, silhouette, portrait, text, writing, numbers, logo, watermark, UI, fewer or more than 25 desks, paired/double desks, cropped furniture, duplicated random doors, door on left, window on right, warped perspective.
```

质检结论：通过。后墙中轴看讲台，左侧整排窗、右侧前后门、5 排 × 5 列单人课桌均可辨认；无人物残留。

## 2. 第九节课红灯教室_空景.png

- 模式：`lighting-weather`
- 编辑目标：`普通教室_空景.png`（锁定同一空间轴与 5 × 5 桌椅布局）
- 灯光参考图：`第二版/第01集_我说我夜盲/clip首尾帧图/clip06_门缝里的第九节课/clip06_首帧.png`
- 最终提示词：

```text
Use case: lighting-weather
Asset type: episode-global empty-location reference anchor for AI comic-video production
Input image 1: edit target; lock its exact empty-classroom camera, geometry, 5-by-5 desk layout, left-window row, two right-side doors, blackboard and lectern.
Input image 2: reference only for the ominous red emergency-lamp plus cold-blue night lighting and semi-realistic Chinese-animation mood.
Primary request: Turn only the time and lighting of Image 1 from daytime into the nighttime “ninth lesson” look from Image 2.
Lighting/mood: deep night outside the left windows; a small red emergency lamp near the front-right wall casts restrained red light; cold blue moonlight enters from the left; subtle red and blue reflections appear on the tiled floor. Ominous but readable.
Constraints: keep Image 1's exact 16:9 rear-wall camera, exactly 25 complete single desks in five columns by five rows, clear center axis, left windows, BOTH right-side doors, blackboard, lectern, walls and all spatial relationships unchanged. Keep the classroom completely empty.
Avoid: any person, teacher, student, head, hand, body, silhouette, ghost, portrait, text, writing, numbers, logo, watermark, UI, added/removed/moved desks, cropped furniture, door or window relocation, mirror reversal, warped perspective.
```

质检结论：通过。与普通教室保持同一空间轴和桌椅布局，仅切换为红色应急灯 + 冷蓝夜光；无人物残留。

## 3. 男生宿舍_空景.png

- 模式：`illustration-story`（参考式生成）
- 风格／夜光参考图：`剧集/第二集/片段06_夜晚宿舍熄灯查寝/首帧.png`；只参考材质、夜光与画风，不沿用人物及旧空间方向
- 最终提示词：

```text
Use case: illustration-story
Asset type: episode-global empty-location reference anchor for AI comic-video production
Input image 1: style, materials, night-lighting and rendering reference only; do not copy its people or its room orientation.
Primary request: Create a completely empty Chinese boys' high-school dormitory at night with a fixed, production-ready spatial axis.
Scene/backdrop: camera stands near the dorm entrance, which is on the RIGHT side of the near wall. Looking straight down a clear central aisle, a rectangular window is centered on the FAR END wall. Metal bunk beds line both the left and right walls, upper and lower bunks, with practical narrow storage and neatly used dark-blue bedding. The story's main bed is the UPPER BUNK of the FIRST bunk group on the LEFT, closest to the far-end window; keep that bed visually identifiable by position but add no labels. Empty beds only.
Style/medium: match Image 1's polished semi-realistic Chinese animation / light urban 2D illustration style, realistic school materials, crisp environmental concept art, subtle lived-in texture.
Composition/framing: landscape 16:9, wide centered establishing shot from near the entrance, one-point perspective down the middle aisle, all important spatial relationships readable.
Lighting/mood: lights out, cold blue moonlight enters from the centered far window; a thin cool-white beam leaks through the right-side entrance door gap. Quiet, tense, but enough detail remains visible.
Constraints: no people anywhere, including under blankets, mirrors, photos or shadows. Maintain entrance-right, window-straight-ahead, bunks-left-and-right, central aisle, main upper bunk first-left-near-window.
Avoid: person, student, body, head, face, hand, silhouette, human-shaped blanket, ghost, portrait, poster, readable writing, text, letters, numbers, logo, watermark, UI, mirrored axis, extra door on left, side-wall window, warped bunk frames, impossible geometry.
```

质检结论：通过。入口在画面右侧、尽头正前为窗、左右上下铺与中央过道明确；冷蓝月光和右侧门缝冷白光正常；无人物或人形被褥。

## 4. 校园厕所_空景.png

- 模式：`illustration-story` 基础生成 + `precise-object-edit` 镜面纠正
- 外部参考图：无
- 基础生成提示词：

```text
Use case: illustration-story
Asset type: episode-global empty-location reference anchor for AI comic-video production
Primary request: Create a completely empty Chinese high-school restroom at night with a fixed, production-ready spatial axis.
Scene/backdrop: From the entrance-area camera, the sink counter spans the FRONT wall straight ahead, with several white basins and one long continuous horizontal mirror above them. A row of closed and partly ajar toilet-stall doors runs along the RIGHT wall. The exit/open doorway is visible at the LEFT REAR. Pale ceramic wall tiles, gray floor tiles, simple metal fixtures, believable clean but slightly aged school construction.
Mirror requirement: The long mirror must show a physically correct reflection of this exact same empty restroom—same basins, tiles, light and empty floor—with no reflected person, face, silhouette, extra corridor, impossible room, or alternate scene.
Style/medium: polished semi-realistic Chinese animation / light urban 2D illustration, matching a serious modern school mystery drama; detailed environmental concept art, realistic proportions and materials, subtle hand-painted finish.
Composition/framing: landscape 16:9, eye-level wide establishing shot, one coherent perspective, sink and mirror dominant at center/front, right stalls and left-rear exit clearly legible.
Lighting/mood: cold white fluorescent night lighting with restrained blue-gray shadows; quiet, uncanny, clean visibility.
Constraints: no people anywhere in the room or mirror. Preserve the front-sink / right-stalls / left-rear-exit axis. Mirror reflection must obey normal optics and remain empty.
Avoid: person, student, body, head, face, hand, silhouette, ghost, portrait, human shadow, writing, text, letters, numbers, restroom signs, logo, watermark, UI, blood, gore, dirt splatter, duplicated sinks, floating fixtures, broken mirror, mirror portal, mismatched or impossible reflection, warped architecture.
```

- 最终镜面修正提示词：

```text
Use case: precise-object-edit
Asset type: episode-global empty-location reference anchor for AI comic-video production
Input image 1: edit target.
Primary request: Correct only the large horizontal mirror reflection. Remove the impossible nested mirror / infinite mirror tunnel.
Mirror edit: The mirror must behave like one ordinary flat wall mirror. It should reflect the empty rear portion of the same restroom behind the camera: plain pale tiled rear wall, the same cold fluorescent ceiling light, a limited natural glimpse of the left-rear exit and right-side stalls according to normal optics. There must be NO second mirror and NO repeated/nested mirror inside it.
Constraints: keep every non-mirror part of Image 1 unchanged—same 16:9 framing, five basins, long sink counter, right-hand stall row, left-rear exit, tiles, lighting, palette and semi-realistic Chinese-animation style. The room and reflection remain completely empty.
Avoid: any person, face, body, silhouette, ghost, portrait, text, logo, watermark, nested mirror, mirror tunnel, recursive reflection, alternate room, impossible reflection, warped architecture.
```

质检结论：通过。正前洗手台和横镜、右侧隔间、左后出口均清晰；镜中为同一空厕所的正常单次反射，无递归镜面、人物或异常空间。

## 文件校验

| 文件 | 尺寸 | SHA-256 |
|---|---:|---|
| `普通教室_空景.png` | 1672 × 941 | `441EB7AE5A5A1307FD201F19678545254922D3CDEF3E07A1B3C2FF2DB4C2C8DC` |
| `第九节课红灯教室_空景.png` | 1672 × 941 | `DC06538E9FF3CDB9C7CF33C402BEE08A4591FB3E4AF5D8A871BFF3688979BE1B` |
| `男生宿舍_空景.png` | 1672 × 941 | `D0C972466858480846F10BF97137D0A7C347717F9781503B8FAE5C1DA5CADD02` |
| `校园厕所_空景.png` | 1672 × 941 | `522B0084573C1A6DDEADE23BD6D3502A7776B58AE808A6760C0DA9598B89A1D3` |
