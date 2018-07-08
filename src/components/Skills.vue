<template>
  <div id="hello">
    {{ name }}

    {{ btnStatus ? 'The button is disabled' : 'The button is active' }}
    <button v-on:click="changeName" v-bind:disabled="btnStatus">Change Name</button>  
  </div>
  
</template>

<script>
  export default {
    name: 'Skills',
    data(){
      return {
        btnStatus : true,
        name: 'Sam Sun'
      }
    } 
  }
</script>
