<template>
  <div class="form">
    <input type="text" placeholder="Name" v-model="user.name">
    <input type="text" placeholder="Surname" v-model="user.surname">
    <input type="number" placeholder="Number" v-model="user.phone">

    <button @click="getValues">Submit</button>
  </div>
</template>

<script>
export default {
  name: "InfoCard",
  data(){
    return{
      user:{
        name:'',
        surname:'',
        phone:'',
      }
    }
  },
  methods:{
    getValues(){
      this.$emit('send-data', this.user)
    }
  }
}
</script>

<style scoped>
.form{
  display: flex;
  flex-direction: column;
  width:200px;
  border:1px solid grey;
  padding: 10px;
}
input{
  margin-bottom: 10px;
  border:1px solid green;
  border-radius: 5px;
  padding: 5px;
}

button{
  border-radius: 5px;
  padding: 5px 10px;
  background-color: white;
  border:1px solid red;
  display: block;
  margin:0 auto;
}
</style>