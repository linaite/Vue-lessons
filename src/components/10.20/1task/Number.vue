<template>
  <div class="buttons">
    <div v-on:click="hideLine" class="button">Mygtukas</div>
  </div>
  <div class="card">
    <h4 class="num">{{ myNumber }}</h4>
    <div v-on:click="addNumber" class="btn">Mygtukas</div>
    <h4>Current number arrived: {{ number }}</h4>
    <div v-if="trigger" class="triggerOn"></div>
  </div>
</template>

<script>
export default {
  name: "number",
  props: {
    number: Number,
  },
  data() {
    return {
      myNumber: 0,
      trigger: true,
    }
  },
  methods: {
    addNumber() {
      this.myNumber += this.number
    },
    hideLine() {
      this.trigger = !this.trigger
    }
  }
}
</script>

<style scoped>
.card {
  border: 1px solid black;
  width: 100px;
  margin-top: 20px;
  padding: 20px;
}

.btn {
  padding: 10px;
  background-color: #42b983;
  border-radius: 10px;
  border: none;
  width: 70px;
}

.button {
 border:1px solid orange;
  padding: 10px;
  width: 100px;
  border-radius: 10px;
  margin-top: 20px;
}

.triggerOn {
  height: 15px;
  background-color: blueviolet;
}

.num{
  text-align: center;
  margin-bottom: 20px;
}
</style>