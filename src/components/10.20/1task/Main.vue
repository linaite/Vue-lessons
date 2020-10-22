<template>
  <div class="text-c">
    <number :number="numbers[0]" />
    <number :number="numbers[1]" />
    <number :number="numbers[2]" />
  </div>
</template>

<script>
import Number from "@/components/10.20/1task/Number";

export default {
  name: 'App',
  components: {
    Number,
  },
  data() {
    return {
      numbers: [5, 10, 25]
    }
  }
  // methods: {
  //   anyName() {
  //     this.number++
  //     if (this.arrOne.length > 0) {
  //       this.arrTwo.push(this.arrOne.pop())
  //     }
  //
  //     console.log(this.arrOne)
  //   }
  // }
}
</script>

<style scoped>
.text-c {
  text-align: center;
}

.num {
  margin-bottom: 20px;
}


</style>