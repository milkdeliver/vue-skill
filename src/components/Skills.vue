<template>
  <div id="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'>{{ index }}. {{ data.skill }}</li>
      </ul>

      <div v-bind:class="{ alert: showAlert, 'another-class': showAnotherClass }"></div>
    </div>
  </div>
  
</template>

<script>
  export default {
    name: 'Skills',
    data(){
      return {
        skills : [
          { "skill": "vue.js"},
          { "skill": "Frontend Developer"}
        ],
        showAlert: true,
        showAnotherClass: true
      }
    } 
  }
</script>

<style scoped>
  .alert {
    background-color: yellow;
    width: 100%;
    height:30px;
  }
  .another-class {
    border: 5px solid black;
  }
</style>
