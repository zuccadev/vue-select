# Install

## NPM
Install the package. _You should install `vue-select@v1.3.3` for use with vue `1.x`._

```bash
$ npm install vue-select
```

Register the component

```js
import Vue from 'vue'
import vSelect from 'vue-select'

Vue.component(vSelect)
```

You may now use the component in your markup

```html
<v-select v-model="selected" :options="['foo','bar']"></v-select>
```

## CDN

Just include `vue` & `vue-select.js` - I recommend using [unpkg](https://unpkg.com/#/).

```html
<script scr="https://unpkg.com/vue@latest"></script>
<!-- use the latest release -->
<script src="https://unpkg.com/vue-select@latest"></script>
<!-- or point to a specific release -->
<script src="https://unpkg.com/vue-select@1.3.3"></script>
```

Then register the component in your javascript:

```js
Vue.component('v-select', VueSelect.VueSelect);
```

You may now use the component in your markup

```html
<v-select v-model="selected" :options="['foo','bar']"></v-select>
```
