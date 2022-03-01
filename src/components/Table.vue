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
      <td :class="colorSaldo">{{ saldoTable }}</td>
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
  },
  computed: {
    colorSaldo() {
      return this.saldoTable >= 200000? 'text-success': 'text-danger'
    }
  }
}
</script>

<style>

</style>