<template>
  <div>
    <button @click="getData">Click</button>
    <h1>Komentariya</h1>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  methods: {
    async getData() {
      try {
        let data = await axios.get('https://jsonplaceholder.typicode.com/users')
        console.log(data.data.name);
      } catch (error) {
        alert(error.message);
      }
    },

  }
}
</script>
<style scoped>
h1 {
  width: 300px;
  margin: 30px auto;
}

button {
  display: block;
  width: 70px;
  padding: 10px;
  margin: 0 auto;
}
</style>