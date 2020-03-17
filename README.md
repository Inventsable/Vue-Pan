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

### Use

```html
<div v-pan.prevent.mouse="panHandle" />
```