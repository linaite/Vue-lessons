<template>
  <div class="h-card">
    <img :src="image" alt="">
    <div class="content">
      {{ text }}
    </div>
  </div>
</template>

<script>
export default {
  name: "HorizontalCard.vue",
  props: {
    image: String,
    text: String,
  }
}
</script>

<style scoped>

.h-card {
  width: 400px;
  height: 200px;
  border: 1px solid black;
  display: flex;
}

.content {
  padding: 10px;
}

div img {
  width: 200px;
  height: 100%;
  background-position: center;
}
</style>