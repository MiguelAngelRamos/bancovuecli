<template>

  <table class="table">
  <thead>
    <tr>
      <th>Saldo</th>
      <th>Estado</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>{{ saldoTable }}</td>
      <td v-if="estadotable">Activo</td>
      <td v-else>Inactivo</td>
    </tr>
  </tbody>
</table>

</template>

<script>
export default {
  props: {
    saldoTable: Number,
    estadotable: Boolean
  }
}
</script>

<style>

</style>