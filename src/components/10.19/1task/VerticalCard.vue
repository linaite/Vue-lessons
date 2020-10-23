<template>
  <div class="v-card">
    <img :src="image" alt="">
    <div class="content">
      {{ text }}
    </div>
  </div>
</template>

<script>
export default {
  name: "VerticalCard.vue",
  props: {
    image: String,
    text: String,
  }
}
</script>

<style scoped>

.v-card {
  width: 200px;
  height: 300px;
  border: 1px solid black;
}

div img {
  width: 100%;
}

</style>