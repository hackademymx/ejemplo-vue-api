<template>
  <main class="user-card">
    <h2>Usuario: {{ user.nombre }}</h2>
    <p>Dirección: {{ user.direccion }} </p>
    <p>Teléfono: {{ user.telefono }} </p>
  </main>
</template>

<script>
export default {
  props:['user']
}
</script>


<style scoped>
.user-card{
-webkit-box-shadow: 10px 10px 5px 0px rgba(207,207,207,1);
-moz-box-shadow: 10px 10px 5px 0px rgba(207,207,207,1);
box-shadow: 10px 10px 5px 0px c;
margin: 25px;
border: 2px solid rgb(112, 112, 112);
border-radius: 15px;
padding: 10px;
}
</style>

