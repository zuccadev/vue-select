# Install

#### Vue Compatibility
- `vue-select ~2.0` is compatible with `vue ~2.0`
- `vue-select ~1.0` is compatible with `vue ~1.0`

## NPM

```shell
# install v2.x for vue 2.x
$ npm install vue-select

# install v1.x for vue 1.x
$ npm install vue-select@1.3.3
```

```html
<template>
   <div>
      <v-select v-model="select" :options="options"></v-select>
   </div>
</template>

<script>
import vSelect from 'vue-select'
export default {
  components: {vSelect},
  data() {
     return {
        selected: null,
        options: ['foo','bar','baz']
     }
  }
}
</script>
```

## CDN/Browser Globals

Just include `vue` & `vue-select.js` - I recommend using [unpkg](https://unpkg.com/#/).

```html
<!-- use the latest release -->
<script src="https://unpkg.com/vue-select@latest"></script>
<!-- or point to a specific release -->
<script src="https://unpkg.com/vue-select@1.3.3"></script>
```
Then register the component in your javascript:

```js
Vue.component('v-select', VueSelect.VueSelect);
```

# Basic Usage
