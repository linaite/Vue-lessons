<template>
  <div v-if="trigger">{{ name }}</div>

  <button @click="changeTrigger">Mygtukas</button>
</template>

<script>
export default {
  name: "FirstComponent",
  props: {
    name: String,
  },
  data(){
    return{
      trigger:false
    }
  },
  methods:{
    changeTrigger(){
      this.trigger = !this.trigger

      // this.$emit('emit-trigger', true)
      this.$emit('betkas', 'labukas visiems!')
    }
  }
}
</script>

<style scoped>
button{
  background-color: coral;
  border-radius: 10px;
  outline: none;
  padding: 7px 15px;
  border: none;
}
</style>