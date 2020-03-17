# vue-pan

Isolated version of [Quasar's](https://github.com/quasarframework/quasar) `v-pan` directive.

## [See demo and API from Quasar docs](https://quasar.dev/vue-directives/touch-pan)

### Installation

```bash
npm i vue-pan
```

Load directive locally:

```html
<script>
  export default {
    directives: {
      "v-pan": require('vue-pan').default
    }
  }
```

Load directive globally:

```js
// in main.js
Vue.directive("v-pan", require('vue-pan').default);

new Vue({
	router,
	render: h => h(App)
}).$mount("#app");
```

### Usage

```html
<div v-pan.prevent.mouse="panHandle" />
```

Returns MouseEvent:
```js
{
  angle: -170.5376777919744,
  center: {x: 48, y: 69},
  changedPointers: [PointerEvent],
  deltaTime: 4216,
  deltaX: -18,
  deltaY: -3,
  direction: 1,
  distance: 18.24828759089466,
  eventType: 4,
  isFinal: true,
  isFirst: false,
  maxPointers: 1,
  offsetDirection: 2,
  overallVelocity: -0.004269449715370019,
  overallVelocityX: -0.004269449715370019,
  overallVelocityY: -0.0007115749525616698,
  pointerType: "mouse",
  pointers: [],
  preventDefault: ƒ (),
  rotation: 0,
  scale: 1,
  srcEvent: PointerEvent {…},
  target: div.input-scroll-field,
  timeStamp: 1584479536981,
  type: "pan",
  velocity: 0,
  velocityX: 0,
  velocityY: 0,
  __proto__: Object,
}
```