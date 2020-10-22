<template>
  <header>
    <nav class="navigation">
      <ul>
        <li>Home</li>
        <li>About</li>
        <li>Contacts</li>
      </ul>
    </nav>
  </header>

</template>

<script>
export default {
  name: "Header.vue"
}
</script>

<style scoped>


header {
  background-color: beige;
  height: 50px;
  display: flex;
  align-items: center;
}

ul {
  display: flex;

  list-style: none;
}

ul li {
  margin-right: 20px;
}

</style>