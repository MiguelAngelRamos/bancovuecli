<template>
  <Navbar />
  <div class="container mt-5 col-sm-6 offset-sm-3">
    <Table/>
  </div>
</template>

/* Instancia Vue */
<script>

import Navbar from './components/Navbar.vue';
import Table from'./components/Table.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Table
  }
}
</script>

<style>

</style>
