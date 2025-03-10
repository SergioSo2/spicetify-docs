---
title: colorExtractor
description: Extracts colors from a playlist, track, album, artist, show, etc.
---

Extracts colors from a playlist, track, album, artist, show, etc.

```ts
function colorExtractor(uri: string): Promise<{
    DESATURATED: string;
    LIGHT_VIBRANT: string;
    PROMINENT: string;
    VIBRANT: string;
    VIBRANT_NON_ALARMING: string;
}>;
```

#### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| uri | `string` | URI of anything that has artwork (playlist, track, album, artist, show, etc.) |

#### Returns

| Name | Type | Description |
| :--- | :--- | :--- |
| DESATURATED | `string` | Desaturated color in hex format. |
| LIGHT_VIBRANT | `string` | Light vibrant color in hex format. |
| PROMINENT | `string` | Prominent color in hex format. |
| VIBRANT | `string` | Vibrant color in hex format. |
| VIBRANT_NON_ALARMING | `string` | Vibrant non alarming color in hex format. |

#### Example

```ts
// Get color from current track
const currentTrack = Spicetify.Player.data.track;
const colors = await Spicetify.ColorExtractor.colorExtractor(currentTrack.uri);
```
