<template>
  <Navbar :titulonav="titulo" :serviciosnav="servicios"/>
  <div class="container mt-5 col-sm-6 offset-sm-3">
    <h3 class="text-center">{{titulo}}</h3>
    <Table :saldoTable="saldo" :estadotable="estado"/>
    <!-- emit -->
    <Button tipobtn="Agregar Saldo" @accion="agregarSaldo"/>
    <Button tipobtn="Disminuir Saldo" @accion="disminuirSaldo" />
  

  </div>
</template>
/* Instancia Vue o Modelo */
<script>
// import Navbar from '@/components/Navbar.vue';
import Navbar from './components/Navbar.vue';
import Table from'./components/Table.vue';
import Button from './components/Button.vue';
export default {
  name: 'App',
  components: {
    Navbar,
    Table,
    Button
  },
  data() {
    return {
      titulo: "BancoVue",
      servicios: ['Prestamos', 'Cuenta Corriente', 'Giros', 'Depositos'],
      saldo: 1000000,
      estado: true,
      fecha: '28-02-2022'
    }
  },
  methods: {
    agregarSaldo() {
      this.saldo = this.saldo + 150000;
    },
    disminuirSaldo() {
      this.saldo = this.saldo - 100000;
    }
  }
}
</script>

/* Estilos Css */
<style>

</style>
