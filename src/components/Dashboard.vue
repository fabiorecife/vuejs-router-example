<template>
  <div>
    <h2>Dashboard</h2>
    <p>Yay you made it!</p>
    <button v-on:click="teste" >Teste</button>
  </div>
</template>
<script>
  import $ from 'jquery'
  export default {
    methods: {
      teste: function () {
        $.get('http://localhost:9101/voto2/status').done(function (data) {
          window.alert(data)
        })
      }
    }
  }
</script>
