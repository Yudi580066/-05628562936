# 写真編集の記録

更新日：2026年10月6日。ユーザー提供の14枚に内蔵画像編集ツール（imagegen）で色調整を行い、WebPへ圧縮。CLI/API経由の生成は使用していません。生成物は実写の色補正を意図したAI編集のため、厳密なピクセル保持ではありません。原本は上書きしていません。

## 配置したファイル

| 画像 | サイズ | 容量 |
| --- | --- | --- |
| [nippon-maru](素材/custom/nippon-maru.webp) | 1269×1240 | 241 KB |
| [minatomirai](素材/custom/minatomirai.webp) | 1536×1024 | 241 KB |
| [chinatown](素材/custom/chinatown.webp) | 1448×1086 | 340 KB |
| [air-cabin](素材/custom/air-cabin.webp) | 1024×1536 | 101 KB |
| [rainbow-bridge](素材/custom/rainbow-bridge.webp) | 1536×1024 | 235 KB |
| [fuji-tv](素材/custom/fuji-tv.webp) | 1536×1024 | 242 KB |
| [ameyoko](素材/custom/ameyoko.webp) | 1536×1024 | 324 KB |
| [ameyoko-sign](素材/custom/ameyoko-sign.webp) | 1448×1086 | 249 KB |
| [landmark-tower](素材/custom/landmark-tower.webp) | 1024×1536 | 186 KB |
| [cosmoworld-night](素材/custom/cosmoworld-night.webp) | 1536×1024 | 377 KB |
| [cosmoworld-rides](素材/custom/cosmoworld-rides.webp) | 1536×1024 | 319 KB |
| [chinatown-lanterns](素材/custom/chinatown-lanterns.webp) | 1024×1536 | 340 KB |
| [redbrick-detail](素材/custom/redbrick-detail.webp) | 1023×1537 | 203 KB |
| [redbrick-panorama](素材/custom/redbrick-panorama.webp) | 1536×1024 | 193 KB |

## 最終編集プロンプト

### nippon-maru

```text
Use case: lighting-weather. Edit target: image 1 (Nippon Maru sailing ship at night, near-square original). Image 2 is ONLY a color and tonal reference, not a scene to combine. This is a real sightseeing website photo. Do subtle photographic color correction only: slightly lift dark midtones, balance whites, retain rich natural blue/cyan skies and warm city lights, moderately crisp contrast and lively but credible saturation to harmonize with reference photo. Preserve exactly image 1's framing, aspect ratio, architecture, every person, object, sign, Japanese lettering, horizon, cables, and fine geometry. Do not invent, remove, repaint or move any object. Do not change time of day/weather. Do not transfer any objects from image 2. Avoid HDR halos, excessive orange/teal, oversaturation, fake textures. Output only one lightly color-corrected version of image 1, no collage, no text overlays.
```

### minatomirai

```text
Use case: lighting-weather. Edit target: image 1 (Minato Mirai skyline with ferris wheel at blue hour, landscape original). Image 2 is ONLY a color and tonal reference, not a scene to combine. This is a real sightseeing website photo. Do subtle photographic color correction only: slightly lift dark midtones, balance whites, retain rich natural blue/cyan skies and warm city lights, moderately crisp contrast and lively but credible saturation to harmonize with reference photo. Preserve exactly image 1's framing, aspect ratio, architecture, every person, object, sign, Japanese lettering, horizon, cables, and fine geometry. Do not invent, remove, repaint or move any object. Do not change time of day/weather. Do not transfer any objects from image 2. Avoid HDR halos, excessive orange/teal, oversaturation, fake textures. Output only one lightly color-corrected version of image 1, no collage, no text overlays.
```

### chinatown

```text
Subtle color correction only, exact same photograph, no changes to sky or objects.
CRITICAL: Do not add or remove clouds or people. Do not replace the sky. Preserve the existing sky color and the source photograph's precise details. The source image is authoritative. Keep this correction barely noticeable.
```

### air-cabin

```text
Subtle color correction only, exact same photograph, no changes to sky or objects.
CRITICAL: Do not add or remove clouds or people. Do not replace the sky. Preserve the existing sky color and the source photograph's precise details. The source image is authoritative. Keep this correction barely noticeable.
```

### rainbow-bridge

```text
Subtle color correction only, exact same photograph, no changes to sky or objects.
CRITICAL: Do not add or remove clouds or people. Do not replace the sky. Preserve the existing sky color and the source photograph's precise details. The source image is authoritative. Keep this correction barely noticeable.
```

### fuji-tv

```text
Use case: lighting-weather. Edit target: image 1 (Fuji Television building in daytime, landscape original). Image 2 is ONLY a color and tonal reference, not a scene to combine. This is a real sightseeing website photo. Do subtle photographic color correction only: slightly lift dark midtones, balance whites, retain rich natural blue/cyan skies and warm city lights, moderately crisp contrast and lively but credible saturation to harmonize with reference photo. Preserve exactly image 1's framing, aspect ratio, architecture, every person, object, sign, Japanese lettering, horizon, cables, and fine geometry. Do not invent, remove, repaint or move any object. Do not change time of day/weather. Do not transfer any objects from image 2. Avoid HDR halos, excessive orange/teal, oversaturation, fake textures. Output only one lightly color-corrected version of image 1, no collage, no text overlays.
```

### ameyoko

```text
Subtle color correction only, exact same photograph, no changes to sky or objects.
CRITICAL: Do not add or remove clouds or people. Do not replace the sky. Preserve the existing sky color and the source photograph's precise details. The source image is authoritative. Keep this correction barely noticeable.
```

### ameyoko-sign

```text
Edit this existing real travel photograph, preserving the exact photographed scene. Make ONLY a very subtle global color/exposure correction: lift midtones at most 0.2 stops, reduce unwanted color cast, give natural colors a small 5% saturation boost and gentle contrast. Keep this a real photograph. Every pixel's subject, geometry, position, camera view, all people, all Japanese sign text, all architecture, lights, clouds and SKY COLOR/TIME OF DAY must remain unchanged. In particular a black night sky must stay black and pale/cloudy skies must stay pale/cloudy. Do not replace the sky, do not create clouds or new lighting, do not relight or reimagine the scene. No stylization, no dramatic cinematic grade. Same exact composition, framing, aspect ratio. Output just the minimally color-corrected source photo.
```

### landmark-tower

```text
Edit this existing real travel photograph, preserving the exact photographed scene. Make ONLY a very subtle global color/exposure correction: lift midtones at most 0.2 stops, reduce unwanted color cast, give natural colors a small 5% saturation boost and gentle contrast. Keep this a real photograph. Every pixel's subject, geometry, position, camera view, all people, all Japanese sign text, all architecture, lights, clouds and SKY COLOR/TIME OF DAY must remain unchanged. In particular a black night sky must stay black and pale/cloudy skies must stay pale/cloudy. Do not replace the sky, do not create clouds or new lighting, do not relight or reimagine the scene. No stylization, no dramatic cinematic grade. Same exact composition, framing, aspect ratio. Output just the minimally color-corrected source photo.
```

### cosmoworld-night

```text
Edit this existing real travel photograph, preserving the exact photographed scene. Make ONLY a very subtle global color/exposure correction: lift midtones at most 0.2 stops, reduce unwanted color cast, give natural colors a small 5% saturation boost and gentle contrast. Keep this a real photograph. Every pixel's subject, geometry, position, camera view, all people, all Japanese sign text, all architecture, lights, clouds and SKY COLOR/TIME OF DAY must remain unchanged. In particular a black night sky must stay black and pale/cloudy skies must stay pale/cloudy. Do not replace the sky, do not create clouds or new lighting, do not relight or reimagine the scene. No stylization, no dramatic cinematic grade. Same exact composition, framing, aspect ratio. Output just the minimally color-corrected source photo.
```

### cosmoworld-rides

```text
Edit this existing real travel photograph, preserving the exact photographed scene. Make ONLY a very subtle global color/exposure correction: lift midtones at most 0.2 stops, reduce unwanted color cast, give natural colors a small 5% saturation boost and gentle contrast. Keep this a real photograph. Every pixel's subject, geometry, position, camera view, all people, all Japanese sign text, all architecture, lights, clouds and SKY COLOR/TIME OF DAY must remain unchanged. In particular a black night sky must stay black and pale/cloudy skies must stay pale/cloudy. Do not replace the sky, do not create clouds or new lighting, do not relight or reimagine the scene. No stylization, no dramatic cinematic grade. Same exact composition, framing, aspect ratio. Output just the minimally color-corrected source photo.
```

### chinatown-lanterns

```text
Edit this existing real travel photograph, preserving the exact photographed scene. Make ONLY a very subtle global color/exposure correction: lift midtones at most 0.2 stops, reduce unwanted color cast, give natural colors a small 5% saturation boost and gentle contrast. Keep this a real photograph. Every pixel's subject, geometry, position, camera view, all people, all Japanese sign text, all architecture, lights, clouds and SKY COLOR/TIME OF DAY must remain unchanged. In particular a black night sky must stay black and pale/cloudy skies must stay pale/cloudy. Do not replace the sky, do not create clouds or new lighting, do not relight or reimagine the scene. No stylization, no dramatic cinematic grade. Same exact composition, framing, aspect ratio. Output just the minimally color-corrected source photo.
```

### redbrick-detail

```text
Edit this existing real travel photograph, preserving the exact photographed scene. Make ONLY a very subtle global color/exposure correction: lift midtones at most 0.2 stops, reduce unwanted color cast, give natural colors a small 5% saturation boost and gentle contrast. Keep this a real photograph. Every pixel's subject, geometry, position, camera view, all people, all Japanese sign text, all architecture, lights, clouds and SKY COLOR/TIME OF DAY must remain unchanged. In particular a black night sky must stay black and pale/cloudy skies must stay pale/cloudy. Do not replace the sky, do not create clouds or new lighting, do not relight or reimagine the scene. No stylization, no dramatic cinematic grade. Same exact composition, framing, aspect ratio. Output just the minimally color-corrected source photo.
```

### redbrick-panorama

```text
Edit this existing real travel photograph, preserving the exact photographed scene. Make ONLY a very subtle global color/exposure correction: lift midtones at most 0.2 stops, reduce unwanted color cast, give natural colors a small 5% saturation boost and gentle contrast. Keep this a real photograph. Every pixel's subject, geometry, position, camera view, all people, all Japanese sign text, all architecture, lights, clouds and SKY COLOR/TIME OF DAY must remain unchanged. In particular a black night sky must stay black and pale/cloudy skies must stay pale/cloudy. Do not replace the sky, do not create clouds or new lighting, do not relight or reimagine the scene. No stylization, no dramatic cinematic grade. Same exact composition, framing, aspect ratio. Output just the minimally color-corrected source photo.
```


## 2026-10-07 提供写真12枚の追加（色調整なし）

神宮前（ハラカド外観・屋上、オモカド外観・鏡の入口）、上野（動物園・国立科学博物館・東京国立博物館）、池袋（アニメイト本店）、渋谷（PARCO）、お台場（ダイバーシティ）、新横浜（ラーメン博物館外観・ラーメンオブジェ）へ提供画像を原ファイルのまま複製。すべて「変更予定」のHTML表示を付与しました。画像自体への文字入れ・色調整・生成は行っていません。
