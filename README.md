# Diatem | Vue SVG Icon

Diatem's Vue 3 SVG icon component, with Vite

## Features

## Installation

```bash
npm i @diatem-net/vue-svg-icon
```

## How to Use

### Global Registration
main.js
```javascript
import SvgIcon from '@diatem-net/vue-svg-icon'
import '@diatem-net/vue-svg-icon/dist/style.css'

createApp(App)
  .use(router)
  .use(TestComponent)
  .mount("#app");
```
#### OR

### Local Registration
HelloWorld.vue
```vue
<script setup>
import SvgIcon from '@diatem-net/vue-svg-icon'
import '@diatem-net/vue-svg-icon/dist/style.css'

<template>
  <SvgIcon name="icon-cart" size="md"/>
</template>

</script>
```
