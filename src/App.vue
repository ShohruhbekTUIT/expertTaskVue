<script>
import { RouterLink, RouterView } from 'vue-router';
import Header from "./components/Header/Header.vue";

export default {
  components: { Header }
}

</script>

<template>
  <Header />
  <!-- <Header :btninfo="{ clas: 'odps-btn', text: 'Отписаться', }" /> -->
  <RouterView />
</template>

<style scoped></style>
