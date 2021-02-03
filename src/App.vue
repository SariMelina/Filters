<template>
  <div class="container">
    <div class="jumbotron">
      <span>
        {{ mensaje | suspensivos | capitalize }}
      </span>
      <hr>
      <span>
        F : {{ temperatura | toF }}
        <br>
        C : {{ temperatura }}
      </span>
    </div>
  </div>
</template>

<script>
export default {  
  data() {
    return {
      mensaje: 'Aprende VueJS fácilmente',
      temperatura: 1
    }
  },
  filters: {
    capitalize(mensaje) {
      return mensaje.toUpperCase()
    },
    toF (value) {
      return value * (9/5) + 32
    }
  }
}

</script>

<style>


</style>
