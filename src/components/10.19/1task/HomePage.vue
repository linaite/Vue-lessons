<template>
  <div class="block">
<!--    <h1>labas vakaras visiems, mano {{myName}}, o mano pavarde {{mySecondName}}!</h1>-->
    <div class="textDiv">Lorem ipsum</div>
<!--    <img :src="catPhoto" alt="">-->
  </div>

</template>

<script>
export default {
  // name: "HomePage.vue",
  props:{
    myName: String,
    mySecondName: String,
    catPhoto: String,
  }
}
</script>

<style scoped>
.textDiv {
  color: green;
}
.block{
  background: antiquewhite;
}

img{
  width:200px;
  height: 200px;
}

</style>