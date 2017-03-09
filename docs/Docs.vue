<style lang="scss">
  @import './assets/scss/docs.scss';

  #sidebar nav {
    // position: fixed;
    // top: 0;
  }
</style>

<template>
  <div id="docs" class="container-fluid">
    <div class="col-md-3" id="sidebar">
      <nav>
        <div class="form-group">
          <label class="control-label">Version</label>
          <v-select id="select-version" v-model="version" :searchable="false" :options="versions"></v-select>
        </div>
        <p v-if="version.v == 'v1'"><small><code>v1.x</code> of <code>vue-select</code> should be used with <code>vue 1.x</code></small></p>
        <sidebar></sidebar>
      </nav>
    </div>
    <div class="col-md-7">
      <article v-html="getDocHtml('install')"></article>
      <v-select v-model="selected" :options="['foo','bar']"></v-select>
      <!-- <article v-html="vModel"></article>
      <article v-html="single"></article>
      <article v-html="reactive"></article>
      <article v-html="labels"></article>
      <article v-html="ajax"></article> -->
    </div>
  </div>
</template>

<script type="text/babel">

/**
 * Note that this file (and anything other than src/components/Select.vue)
 * has nothing to do with how you use vue-select. These files are used
 * for the demo site at http://sagalbot.github.io/vue-select/.
 */

// import Examples from './components/Examples.vue'
// import Params from './components/Params.vue'
// import Ajax from './components/snippets/Ajax.vue'

const docs = {
  'v1.x': {
    install: require('./md/v2/install/Install.md'),
    vModel: require('./md/VModel.md'),
    single: require('./md/SingleMultiple.md'),
    reactive: require('./md/ReactiveOptions.md'),
    labels: require('./md/CustomLabels.md'),
    ajax: require('./md/Ajax.md'),
  },
  'v2.x': {
    install: require('./md/v2/install/Install.md'),
    vModel: require('./md/VModel.md'),
    single: require('./md/SingleMultiple.md'),
    reactive: require('./md/ReactiveOptions.md'),
    labels: require('./md/CustomLabels.md'),
    ajax: require('./md/Ajax.md'),
  }
}

export default {
  // components: { Params, Examples, Ajax }
  data () {
    return {
      docs,
      versions: ['v1.x','v2.x'],
      version: 'v2.x'
    }
  },

  methods: {
    getDocHtml(doc) {
      return this.docs[this.version][doc]
    }
  }
}
</script>
