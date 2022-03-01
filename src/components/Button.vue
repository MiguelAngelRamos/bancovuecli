<template>
 <!-- <h3>Los botones</h3> -->
  <button :class="colorBoton" v-on:click="accionBtn">{{ tipobtn }}</button>
</template>

<script>
export default {
  props: {
    tipobtn: String
  },
  computed: {
    colorBoton() {
      return this.tipobtn ==="Agregar Saldo"? 'btn btn-success': 'btn btn-danger'
    }
  },
  methods: {
    accionBtn() {
      this.$emit('accion');
    }
  }
}
</script>

<style scoped>
 button {
   margin-right: 5px;
 }

 /* h3 {
   color: red;
 } */
</style>