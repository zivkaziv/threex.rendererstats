@zivkaziv/three-renderer-stats
========================================
Without Require() and module.exports

FORKED FROM https://github.com/xailabs/threex.rendererstats

- Allow reset by calling `update()` without passing renderer
- Published on npm
- Fix programs count <a href="https://github.com/jeromeetienne/threex.rendererstats/pull/4" target="_blank">(~ PR4)</a>

========================================

It is a three.js extension to display realtime informations about ```THREE.WebGLRenderer```.
Here is a [basic example](http://jeromeetienne.github.io/threex.rendererstats/examples/basic.html). It is widely inpired from @mrdoob [stats.js](https://github.com/mrdoob/stats.js/).
It is released under MIT license.

## How To install it

Via yarn:
```javascript
yarn add @zivkaziv/three-renderer-stats
```

Via npm:
```javascript
npm install @zivkaziv/three-renderer-stats --save
```

## How To Use It

```javascript
import RendererStats from '@zivkaziv/three-renderer-stats';
const rendererStats = new RendererStats();
```

position it on the page with css with something along this line:

```javascript
rendererStats.domElement.style.position	= 'absolute'
rendererStats.domElement.style.left	= '0px'
rendererStats.domElement.style.bottom	= '0px'
document.body.appendChild( rendererStats.domElement )
```

finally update it at every frame, passing the webGLRenderer reference:

```javascript
rendererStats.update(renderer);
```


update it without passing anything (or passing something falsy) to reset the displayed output:

```javascript
rendererStats.update(null);
```