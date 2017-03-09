<template>
<ul class="nav nav-pills nav-stacked">
  <li v-for="(value, key, index) in nav">
    <a href="#">{{ value.title }}</a>
    <ul v-if="value.children">
      <li v-for="(value, key, index) in value.children">
        {{ value }}
      </li>
    </ul>
  </li>
    <!-- <li>
        <a href="#">Install &amp; Usage</a>
        <ul>
            <li><a href="#">NPM</a></li>
            <li><a href="#">CDN</a></li>
        </ul>
    </li>
    <li>
        <a href="#">Features</a>
        <ul>
            <li><a href="#">Value Syncing</a></li>
            <li><a href="#">Single/Multiple</a></li>
            <li><a href="#">Tagging</a></li>
            <li><a href="#">Searching</a></li>
            <li><a href="#">TypeAhead</a></li>
            <li><a href="#">Ajax Support</a></li>
            <li><a href="#">Vuex Support</a></li>
        </ul>
    </li>
    <li>
        <a href="#">Component Events</a>
        <ul>
            <li><a href="#">search:focus</a></li>
            <li><a href="#">search:blur</a></li>
            <li><a href="#">input</a></li>
            <li><a href="#">pointer:up</a></li>
            <li><a href="#">pointer:down</a></li>
        </ul>
    </li>
    <li>
        <a href="#">Props</a>
        <ul>
            <li>

            </li>
        </ul>
    </li>
    <li>
        <a href="#">Examples</a>
        <ul>
            <li><a href="#">NPM</a></li>
            <li><a href="#">CDN</a></li>
        </ul>
    </li>
    <li><a href="#">Ajax</a></li>
    <li><a href="#">Parameters</a></li> -->
</ul>
</template>

<script>
import nav from '../data/navigation'
export default {
  data() {
    return {
      nav
    }
  }
}
</script>
