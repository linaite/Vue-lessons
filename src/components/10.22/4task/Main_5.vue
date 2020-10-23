<template>
  <div class="block">
    <InfoCard @send-data="getData"/>
    <div class="card">
      <h2>{{ user.name }}</h2>
      <h2>{{ user.surname }}</h2>
      <h2>{{ user.phone }}</h2>
    </div>
  </div>
</template>

<script>
import InfoCard from "@/components/10.22/4task/InfoCard";

export default {
  name: "Main_5",
  components: {
    InfoCard
  },
  data() {
    return {
      user: {
        name: '',
        surname: '',
        phone: '',
      }
    }
  },
  methods: {
    getData(data) {
      this.user = data
    }
  }
}
</script>

<style scoped>
.card{
  border:1px solid black;
  padding: 10px;
  width:200px;
  height: 150px;
}
.block{
  display: flex;
  justify-content: space-around;
}
</style>