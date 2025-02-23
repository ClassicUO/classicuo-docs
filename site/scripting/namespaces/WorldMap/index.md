## Classes

<div class="heading-level-3">
<a id="worldmap" name="worldmap"></a>

### WorldMap

#### Properties

<div class="heading-level-5">
<a id="markers" name="markers"></a>

##### markers

```ts
markers: readonly WorldMapMarker[];
```

Gets list of World Map markers.

**Note:** this list is readonly, use `addMarker` or `removeMarker` to manage the World Map markers.

</div>

#### Methods

<div class="heading-level-5">
<a id="addmarker" name="addmarker"></a>

##### addMarker()

```ts
addMarker(marker: WorldMapMarker | WorldMapMarkerPartial): WorldMapMarker
```

Adds a marker to the World Map.

###### Parameters

| Parameter | Type                                                                                                     | Description |
| :-------- | :------------------------------------------------------------------------------------------------------- | :---------- |
| `marker`  | [`WorldMapMarker`](index.md#worldmapmarker) \| [`WorldMapMarkerPartial`](index.md#worldmapmarkerpartial) |             |

###### Returns

[`WorldMapMarker`](index.md#worldmapmarker)

###### Example

```ts
const marker = worldMap.addMarker({ name: 'Here', x: player.x, y: player.y, color: 'green' });
```

</div>

---

<div class="heading-level-5">
<a id="close" name="close"></a>

##### close()

```ts
close(): void
```

Closes the World Map gump.

###### Example

```ts
worldMap.close();
```

</div>

---

<div class="heading-level-5">
<a id="goto" name="goto"></a>

##### goTo()

```ts
goTo(coords: object): void
```

Changes the current location of the World Map, which also enables Free View.

###### Parameters

| Parameter  | Type     | Description |
| :--------- | :------- | :---------- |
| `coords`   | `object` |             |
| `coords.x` | `number` | -           |
| `coords.y` | `number` | -           |

###### Example

```ts
worldMap.goTo({ x: player.x, y: player.y });
```

</div>

---

<div class="heading-level-5">
<a id="open" name="open"></a>

##### open()

```ts
open(): void
```

Opens the World Map gump.

###### Example

```ts
worldMap.open();
```

</div>

---

<div class="heading-level-5">
<a id="parselocation" name="parselocation"></a>

##### parseLocation()

```ts
parseLocation(input: string): undefined | object
```

Attempts to parse a location string and convert into map coordinates.

**Note:** Currently only supports Sextant coordinates, e.g. `100o25'S,40o04'E`

###### Parameters

| Parameter | Type     | Description |
| :-------- | :------- | :---------- |
| `input`   | `string` |             |

###### Returns

`undefined` | `object`

###### Example

```ts
const marker = worldMap.addMarker({
  name: 'Sextant Loc',
  color: 'green',
  ...worldMap.parseLocation("100o25'S,40o04'E")
});
```

</div>

---

<div class="heading-level-5">
<a id="removeallmarkers" name="removeallmarkers"></a>

##### removeAllMarkers()

```ts
removeAllMarkers(): void
```

Removes all World Map markers.

</div>

---

<div class="heading-level-5">
<a id="removemarker" name="removemarker"></a>

##### removeMarker()

```ts
removeMarker(marker: string | object): boolean
```

Remove a marker from the World Map.

###### Parameters

| Parameter | Type                 | Description |
| :-------- | :------------------- | :---------- |
| `marker`  | `string` \| `object` |             |

###### Returns

`boolean`

###### Example

```ts
worldMap.removeMarker('Here');
```

</div>
</div>

## Interfaces

<div class="heading-level-3">
<a id="worldmapmarker" name="worldmapmarker"></a>

### WorldMapMarker

#### Properties

<div class="heading-level-5">
<a id="color" name="color"></a>

##### color

```ts
color: string;
```

Color of the marker, e.g. "blue"

</div>

---

<div class="heading-level-5">
<a id="mapid" name="mapid"></a>

##### mapId

```ts
mapId: number;
```

Map Index/Id to place the marker on

</div>

---

<div class="heading-level-5">
<a id="name" name="name"></a>

##### name

```ts
name: string;
```

Name of the marker

</div>

---

<div class="heading-level-5">
<a id="x" name="x"></a>

##### x

```ts
x: number;
```

X coordinate

</div>

---

<div class="heading-level-5">
<a id="y" name="y"></a>

##### y

```ts
y: number;
```

Y coordinate

</div>

---

<div class="heading-level-5">
<a id="zoomlevel" name="zoomlevel"></a>

##### zoomLevel

```ts
zoomLevel: number;
```

ZoomLevel at which the marker appears

</div>
</div>

---

<div class="heading-level-3">
<a id="worldmapmarkerpartial" name="worldmapmarkerpartial"></a>

### WorldMapMarkerPartial

#### Properties

<div class="heading-level-5">
<a id="color-1" name="color-1"></a>

##### color?

```ts
optional color: string;
```

</div>

---

<div class="heading-level-5">
<a id="mapid-1" name="mapid-1"></a>

##### mapId?

```ts
optional mapId: number;
```

</div>

---

<div class="heading-level-5">
<a id="name-1" name="name-1"></a>

##### name

```ts
name: string;
```

</div>

---

<div class="heading-level-5">
<a id="x-1" name="x-1"></a>

##### x

```ts
x: number;
```

</div>

---

<div class="heading-level-5">
<a id="y-1" name="y-1"></a>

##### y

```ts
y: number;
```

</div>

---

<div class="heading-level-5">
<a id="zoomlevel-1" name="zoomlevel-1"></a>

##### zoomLevel?

```ts
optional zoomLevel: number;
```

</div>
</div>
