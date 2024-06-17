# Preview 

https://benchmark.webgl.gezilinll.com/

# WebGL Libraries Benchmark

Based on [canvas-engines-comparison](https://github.com/slaylines/canvas-engines-comparison)

- Up to 10000 different rectangles moving on a canvas with various speed
- Different choice of libraries used to render the scene :

# What's different

* More comparison
  * CanvasRenderingContext2D / Babylon.js

* More test case
  * Rect / Image / Text

* More specific comparison
  * PixiJS：add Sprite/SpriteContainer compare with Rect
  * CanvasKit-wasm：add immediately compare with batch
* More control variable
  * Cache random result to make sure every library use same data to render

* Use TypeScript
* Use newest version of dependencies

## Tested Result

FPS of render 10000 elements

| Type/Library | Pixi.js                                | CanvasKit | Context2D | Konva.js | Three.js         | Babylon.js       | Fabric.js | DOM  |
| ------------ | -------------------------------------- | --------- | --------- | -------- | ---------------- | ---------------- | --------- | ---- |
| Rect         | 23: Graphics<br />60: SpiriteContainer | 30        | 27        | 23       | 10(optimizable?) | 13(optimizable?) | 10        | 11   |
| Image        | 20                                     | 30        | 31        |          |                  |                  |           |      |
| Text         | 10: Text<br />60: SpiriteContainer     | 27        | 25        | 15       |                  |                  |           |      |

## Quick Start

```
$ yarn install
$ yarn build
$ yarn start
```

## Misc

A list of webgl libraries : https://gist.github.com/dmnsgn/76878ba6903cf15789b712464875cfdc
