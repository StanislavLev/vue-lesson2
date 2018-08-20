<template>
  <div id="app-root">
    <header><h1>{{title}}</h1></header>
    <div class="puppy-name-grid">
      <puppy v-for="(puppy_name, index) in names" v-bind:name="puppy_name" v-bind:index="index+1" v-bind:key="index"></puppy>
    </div>
  </div>
</template>

<script>

import Puppy from './components/Puppy.vue'

export default {
  components: {
    'puppy': Puppy
  },
  data() {
    return {
      title: "Puppy Story Tellers!",
      names: ['Lucy', 'Rocky', 'Daisy', 'Buddy', 'Lola', 'Luna', 'Bear', 'Duke', 'Sophie', 'Tucker']
    }
  }
}
</script>
