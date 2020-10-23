<template>
  <div class="inputHolder">
    {{ inputvalue }}
    <input type="text" v-model="inputvalue" placeholder="Type here...">
    <button @click="log">Get input value</button>
  </div>
</template>

<script>
export default {
  name: "Inputs",
  data() {
    return {
      inputvalue: null
    }
  },
  methods: {
    log() {
      console.log(this.inputvalue)
    }
  }
}
</script>

<style scoped>
input {
  padding: 5px;
}
</style>