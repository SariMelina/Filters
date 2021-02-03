<template>
  <div class="container">
    <div class="jumbotron">
      <span>
        {{ mensaje | suspensivos }}
      </span>
      <hr>
      <span>
        {{ mensaje }}
      </span>
    </div>
  </div>
</template>

<script>
export default {  
  data() {
    return {
      mensaje: 'Aprende VueJS fácilmente'
    }
  },
  filters: {
    capitalize(mensaje) {
      return mensaje.toUpperCase()
    }
  }
}

</script>

<style>


</style>
