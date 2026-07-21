# 场景生成记录 B

## 生成方式

- 模式：内置 `image_gen`（默认生成模式）
- 用途：第二版十集在“新建集 · 开场设置”中的全局空间锚点
- 统一规格：横版 16:9，实际输出均为 1672 × 941 PNG
- 统一限制：空景、无人物、无人物倒影、无可读文字、无 Logo、无水印
- 质检方式：每张生成后均以原始分辨率打开检查人物、可读乱码、空间左右关系、镜像、Logo 与水印

## 1. 荣誉墙走廊_空景.png

最终提示词：

```text
Use case: illustration-story
Asset type: episode-global empty-environment reference anchor for a suspense school animation
Primary request: Create a clean 16:9 landscape establishing shot of an older Chinese high-school honor-wall corridor, with absolutely no people.
Scene/backdrop: A long corridor in strict one-point perspective. Along the LEFT wall, a continuous series of glass-fronted honor display cabinets containing awards and small student-photo placeholders; every paper, plaque, portrait, and caption inside must be deliberately soft, tiny, abstract, and impossible to read. Along the RIGHT wall, a row of school windows. High overhead near the ceiling is one old wall-mounted broadcast loudspeaker. At the far end, a plain door and branching passage subtly indicate the direction of the infirmary, but there is no readable sign.
Style/medium: polished semi-realistic Chinese manhua / 2D animated drama background, grounded architecture, realistic materials, clean cinematic linework, matching a contemporary urban-school supernatural suspense series.
Composition/framing: wide horizontal 16:9, eye-level, clear spatial continuity and navigable geometry, foreground-to-background depth, no Dutch angle, no mirrored layout; LEFT is the display-cabinet side and RIGHT is the window side.
Lighting/mood: cold white daytime fluorescent light mixed with pale window light; quiet, slightly clinical and ominous, no dramatic fog.
Color palette: desaturated gray-blue, aged cream walls, muted wood and metal, small restrained dark red accents only.
Constraints: EMPTY scene; no human, no silhouette, no face, no reflection of a person, no readable writing, no letters, no numbers, no signage, no logo, no watermark, no border, no interface elements. All photo and certificate contents must remain blurry abstract thumbnail blocks. Do not swap left and right.
Avoid: characters, crowds, legible Chinese or English, poster typography, excessive horror gore, fisheye distortion, impossible geometry, extra doors blocking the corridor.
```

质检：通过。左侧连续玻璃荣誉柜、右侧窗、顶端旧喇叭、走廊尽头门与冷白日间光均正确；证书与照片仅为不可读缩略块；无人物、无可读文字、无镜像、无 Logo、无水印。

## 2. 医务室_空景.png

最终提示词：

```text
Use case: illustration-story
Asset type: episode-global empty-environment reference anchor for a suspense school animation
Primary request: Create a clean 16:9 landscape establishing shot looking inward from the entrance of an older Chinese high-school infirmary, with absolutely no people.
Scene/backdrop: From the doorway, the LEFT side holds a tall filing cabinet for medical records with many plain unlabeled drawers. The RIGHT side holds a simple examination bed with a white sheet. A worn wooden desk stands near the CENTER with a small adjustable examination lamp. On the far BACK wall, directly ahead, is a plain tall white refrigerated medical-storage cabinet. On the RIGHT wall, hang a simple eye-test chart made only of blurred abstract gray blocks; it must not contain readable symbols, letters, numbers, or words. Include plausible sink, medicine cabinet, and aged institutional details without cluttering the central aisle.
Style/medium: polished semi-realistic Chinese manhua / 2D animated drama background, grounded school architecture, realistic materials, clean cinematic linework, contemporary urban-school supernatural suspense tone.
Composition/framing: wide horizontal 16:9, eye-level entrance viewpoint, strong depth, clear left-right placement, central aisle leading to the rear white cabinet, no Dutch angle, no mirrored layout.
Lighting/mood: cold white fluorescent, faint sickly green-gray cast, clinical and unsettling but not gory, clean readable geometry.
Color palette: desaturated white, pale gray-green, muted wood brown, cool blue shadows.
Constraints: EMPTY scene; no human, no silhouette, no patient, no reflection of a person. No readable writing, no letters, no numbers, no labels, no signage, no logo, no watermark, no border, no interface. LEFT filing cabinet, RIGHT examination bed, CENTER wooden desk and lamp, BACK white refrigerator, RIGHT-wall blurred chart. Do not swap left and right.
Avoid: characters, legible eye-chart symbols, posters with text, hospital branding, blood, gore, messy fantasy equipment, fisheye distortion, impossible geometry.
```

质检：通过。入口视角、左病历柜、右检查床、中间木桌与检查灯、后墙白色冷柜、右墙模糊视力图均正确；无人物、无可读文字、无镜像、无 Logo、无水印。

## 3. 夜间操场_空景.png

初始生成提示词：

```text
Use case: illustration-story
Asset type: episode-global empty-environment reference anchor for a suspense school animation
Primary request: Create a clean 16:9 high-angle wide establishing shot of an empty Chinese high-school sports field at midnight, with strict spatial geography and absolutely no people.
Scene/backdrop: A red oval running track surrounds a green central field. At the FAR END in the CENTER stands a low concrete rostrum / school assembly stage facing the field. At the LEFT REAR edge is the visible entrance path toward the dormitory building. At the RIGHT REAR edge is the visible entrance path toward the teaching building. Beyond the RIGHT SIDELINE, outside the track, sits a low single-story sports equipment-room structure whose plain metal door faces inward toward the field. A few chain-link fences and sparse campus trees establish the perimeter.
Style/medium: polished semi-realistic Chinese manhua / 2D animated drama background, grounded contemporary school architecture, realistic materials, restrained clean cinematic linework, supernatural suspense tone.
Composition/framing: wide horizontal 16:9 from an elevated corner viewpoint, clearly show the whole track loop, central field, centered far rostrum, dorm entry left-rear, teaching-building entry right-rear, and equipment-room door along the right sideline. Stable horizon, no Dutch angle, no mirrored layout.
Lighting/mood: cold blue moonlight and sparse dim campus lamps; one very subtle dark-red emergency lamp glows beside the FAR CENTER rostrum, casting a small restrained red accent. Quiet, deserted, ominous, readable silhouettes and geometry.
Color palette: deep navy and slate blue, muted track red, dark green field, tiny controlled red emergency-light accent.
Constraints: EMPTY scene; no human, no student, no guard, no silhouette, no face, no crowd. No readable writing, no letters, no numbers, no banners, no scoreboard text, no logo, no watermark, no border, no interface. Preserve the side assignments exactly: dorm LEFT REAR, teaching building RIGHT REAR, equipment room OUTSIDE RIGHT SIDELINE with its door facing the field, rostrum FAR CENTER.
Avoid: swapped left/right, daytime, stadium spectacle, packed bleachers, athletes, vehicles, gore, neon cyberpunk, heavy fog hiding geometry, fisheye distortion, impossible track layout.
```

初检修订：初始图的空间关系正确，但教学楼窗户、校园路灯和器材室门灯亮着，与第 7 集“全校停电”设定冲突，因此以初始图为编辑目标进行了仅限照明状态的修订。

最终参考编辑提示词：

```text
Use case: lighting-weather
Asset type: corrected episode-global empty-environment reference anchor
Input image: Image 1 is the edit target. Preserve its exact composition, camera, buildings, track, field, rostrum, trees, fences, equipment-room geometry, and every object position.
Primary request: Depict a total campus power outage. Change lighting only.
Required edit:
- Turn OFF every lit window in both the left dormitory building and the right teaching building; all windows must be fully dark and unlit.
- Turn OFF every white campus lamp, road lamp, track lamp, building entrance light, and pathway light throughout the image.
- Turn OFF the white exterior light on the right-side equipment room; its door and wall must be dark.
- Remove all artificial white light pools and white glows.
- Keep ONLY natural cold blue moonlight from the moon and exactly ONE dim dark-red emergency light mounted at the far-center rostrum.
- The field, track, buildings, equipment room, roads and trees must remain visible only through restrained cold-blue moonlight, with the single small red rostrum accent.
Invariants: change only the lighting state. Keep the original 16:9 framing and pixel composition; keep the far-center rostrum, left-rear dormitory, right-rear teaching building, and low equipment room outside the right sideline in exactly the same locations, sizes, shapes, and perspective. Keep the scene empty.
Constraints: no people, silhouettes, faces, vehicles, readable writing, logo, watermark, border, or interface. No new objects. No rearrangement. No crop. No mirroring.
Avoid: any glowing building window, any white lamp point, any equipment-room porch light, any bright road, any additional red light, excessive darkness that erases the track geometry, fog, lightning, neon effects.
```

最终质检：通过。全校建筑窗户、操场及道路白色路灯、建筑入口灯与器材室白灯均已熄灭；仅保留冷蓝月光和远端中央主席台的一盏暗红应急灯。高位广角、远端中央主席台、环形跑道、左后宿舍、右后教学楼及右侧边线外器材室的位置与构图保持一致；无人物、无可读文字、无镜像、无 Logo、无水印。

## 4. 器材室_空景.png

最终提示词：

```text
Use case: illustration-story
Asset type: episode-global empty-environment reference anchor for a suspense school animation
Primary request: Create a clean 16:9 interior anchor of an empty old school sports equipment room at night, with strict spatial geography and absolutely no people.
Scene/backdrop: Camera is positioned in the DEEP RIGHT-REAR CORNER of the room, looking diagonally toward the LEFT-FRONT. At the LEFT-FRONT is a heavy plain metal entrance door with one narrow vertical wired-glass window. The door opens toward the sports field; dim RED light leaks through its window and around its threshold from outside. Along the LEFT WALL is a sturdy open rack holding basketballs, footballs, and a few plain training cones with no markings. Against the BACK WALL are neatly stacked dark folding gym mats. Along the RIGHT WALL are tall worn gray steel storage cabinets; high above them is one old wall-mounted broadcast loudspeaker. Keep a clear CENTRAL AISLE through the room from foreground to the metal door.
Style/medium: polished semi-realistic Chinese manhua / 2D animated drama background, grounded contemporary school architecture, realistic worn metal, rubber, canvas and concrete textures, clean cinematic linework, supernatural suspense tone.
Composition/framing: wide horizontal 16:9, deep right-rear viewpoint toward left-front door, moderate wide angle without distortion; spatial layout must be unmistakable and physically plausible. No Dutch angle and no mirrored layout.
Lighting/mood: dim cold blue interior moonlight and weak overhead spill; controlled dark red exterior glow enters only from the metal door area, creating ominous blue-red contrast while preserving visible geometry.
Color palette: slate blue, charcoal gray, aged green-gray metal, muted rubber colors, restrained dark red light.
Constraints: EMPTY scene; no human, no student, no guard, no silhouette, no face, no human reflection. No readable writing, no letters, no numbers, no labels, no logo, no watermark, no border, no interface. Preserve exact positions: door LEFT-FRONT, ball rack LEFT WALL, folded mats BACK WALL, gray cabinets and high loudspeaker RIGHT WALL, clear CENTER aisle.
Avoid: swapped or mirrored layout, open exterior view showing people, sports-brand markings, poster text, random weapons, gore, excessive fog, fisheye distortion, clutter blocking the aisle, impossible shelves.
```

质检：通过。右后深处向左前视角、左前金属门与窄窗、左墙球架、后墙折叠垫、右墙灰柜与高处喇叭、中央通道均正确；门外红光与室内冷蓝光正确；无人物、无可读文字、无镜像、无 Logo、无水印。
