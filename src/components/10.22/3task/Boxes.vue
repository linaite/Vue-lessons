<template>
  <div class="card">
    <div class="boxes">
      <div v-if="stringLength<20" class="box">A</div>
      <div v-else class="box">B</div>
    </div>

  </div>
</template>

<script>
export default {
  name: "Boxes",
  props: {
    stringLength: Number,
  },
  data() {
    return {
      // imValue: "",
    }
  }
}
</script>

<style scoped>
.card {
  width: 300px;
  border: 7px solid red;
  padding: 10px;
}

.boxes {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}

.box {
  width: 100px;
  height: 100px;
  border: 1px solid black;
  display: flex;
  align-items: center;
  justify-content: center;
}

</style>