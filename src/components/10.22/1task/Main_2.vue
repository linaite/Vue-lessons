<template>
  <!--  <FirstComponent :name="myName" @emit-trigger="changeState"/>-->

  <FirstComponent :name="myName" @betkas="sayHello"/>
  {{ textArrived }}
  <div class="colorDiv" v-if="showBox"></div>

  <img :src="cat[0]" alt="">
  <Cards/>
</template>

<script>

import FirstComponent from "@/components/10.22/1task/FirstComponent";
import Cards from "@/components/10.22/2task/Cards";

export default {
  name: "Main",
  components: {
    Cards,
    FirstComponent
  },
  data() {
    return {
      myName: "Lina",
      showBox: false,
      textArrived: null,
      nums:0,
      cats:[

      ]
    }
  },
  methods: {
    changeState() {
      this.showBox = !this.showBox
    },
    sayHello(textFromEvent) {
      this.textArrived = textFromEvent
    },
    changePhoto(){

    }
  }
}
</script>

<style scoped>
.colorDiv {
  height: 200px;
  width: 300px;
  background-color: aqua;
}
</style>