<template>
  <Boxes :stringLength="imValue.length"/>
<!--  <input type="text" placeholder="Type smth..." v-model="imValue">-->
<!--  <Inputs/>-->
  <input type="text" placeholder="Type smth..." v-model="imValue">
</template>

<script>
// import Inputs from "@/components/10.22/3task/Inputs";
import Boxes from "@/components/10.22/3task/Boxes";

export default {
  name: "Main_4",
  components: {
    // Inputs,
    Boxes,
  },
  data(){
    return{
      imValue: "",
    }
  }

}
</script>

<style scoped>

</style>