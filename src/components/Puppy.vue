<template>
  <div class="puppy-section"> 
    <h3>Hi I'm {{name}} and this is my story...</h3>
    <p><img class="item1" v-bind:src="imgURL" alt="puppy image" />Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true
    },
    index: {
      type: Number,
      required: true
    },
  },
  computed: {
    imgURL() {
      return 'http://www.placepuppy.net/'+this.index+'p/150/125';
    }
  }
}
</script>

<style scoped>

h3 {
  text-align: center;
  margin-bottom: 0;
}

img {
  float: left;
  margin: 0 10px 5px 0;
}

p {
  line-height:1.2em;
  height:12em;
  overflow:hidden;
  text-overflow: ellipsis;
}

.puppy-section{
  box-shadow: 0 0 20px rgba(0,0,0,0.2);
  padding: 10px;
  width: 300px;
}
</style>