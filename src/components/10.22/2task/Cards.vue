<template>
  <div class="card">
    <img :src="photo[nums]" alt="">
    <div class="content">
      <div class="btns">
        <button v-on:click="changePhoto(true)">Previous</button>
        <button v-on:click="changePhoto(false)">Next</button>
      </div>
      <div class="btns">
        <button @click="triggerSmth('cat')" class="bg-green">Get cats</button>
        <button @click="triggerSmth('dog')" class="bg-green">Get dogs</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Cards",
  data() {
    return {
      nums: 0,
    }
  },
  props: {
    photo: Array,
    name: String,
  },
  methods: {
    changePhoto(direction) {
      if (direction) {
        if (this.nums < this.photo.length - 1) {
          this.nums++
        } else {
          this.nums = 0
        }
      } else {
        if (this.nums > 0) {
          this.nums--
        } else {
          this.nums = this.photo.length - 1
        }
      }
    },

    triggerSmth(value) {
      this.$emit('my-event', value)
    }
  }
}
</script>

<style scoped>
.card {
  width: 300px;
  box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.75);
}

.card img {
  width: 100%;
  height: 250px;
}

.content {
  padding: 10px;
}

button {
  width: 100px;
  background-color: lightgray;
  border-radius: 10px;
  border: none;
  padding: 10px;
  outline: none
}

.btns {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}
.bg-green{
  background-color: green;
  color:white;
}
</style>