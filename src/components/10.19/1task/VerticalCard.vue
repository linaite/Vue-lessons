<template>
  <div class="v-card">
    <img :src="img" alt="">
    <div class="content">
      {{ content }}
    </div>
  </div>
</template>

<script>
export default {
  name: "VerticalCard.vue",
  props: {
    img: String,
    content: String,
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