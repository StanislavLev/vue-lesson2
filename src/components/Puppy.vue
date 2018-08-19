<template>
  <button v-on:click="changeURL"><h3>{{name}}</h3></button>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true
      }
  },
  methods: {
    changeURL(){
      this.$emit('changeURL', this.name);
    }
  }
}
</script>


