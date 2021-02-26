# phaser3-game-template
A simple game template using Phaser3, React and TypeScript

## How to extrude tile images
https://github.com/sporadic-labs/tile-extruder

1. Install tile-extruder
`npm install --global tile-extruder`

2. Extrude image
`tile-extruder --tileWidth 32 --tileHeight 32 --margin 2 --spacing 2 --input ./src/assets/img/tilesheet.png --output ./src/assets/img/tilesheet-extruded.png`

3. Use tileset
```ts
const tileSize = 32;

const map = this.make.tilemap({
    key: 'map',
    tileWidth: tileSize,
    tileHeight: tileSize,
});

const tiles = map.addTilesetImage('map', 'tilesheet', tileSize, tileSize, 1, 2);
```
