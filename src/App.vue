<template>
  <div id="app-root">
    <header><h1>{{title}}</h1></header>
    <div class="puppy-name-grid">
      <puppy v-for="(puppy_name, index) in names" v-bind:name="puppy_name" v-bind:key="index" v-on:changeURL="updateURL($event)"></puppy>
    </div>
    <h2>Hi, I'm {{current_puppy}}</h2>
    <img v-bind:src="puppy_url" alt="puppy image" />  
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
      title: "Hello VUE! Puppy slideshow!",
      current_puppy: 'Lucy',
      puppy_url : "http://www.placepuppy.net/1p/760/475",
      names: ['Lucy', 'Rocky', 'Daisy', 'Buddy', 'Lola', 'Luna', 'Bear', 'Duke', 'Sophie', 'Tucker']
    }
  },
  methods: {
    updateURL(puppy_name) {
      this.current_puppy = puppy_name;
      this.puppy_url = "http://www.placepuppy.net/" + (this.names.indexOf(puppy_name)+1) + "p/760/475";
    }
  }
}
</script>
