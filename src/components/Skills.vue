<template>
  <div id="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'>{{ index }}. {{ data.skill }}</li>
      </ul>

      <div v-bind:class="{ alert: showAlert }"></div>
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
        showAlert: true

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

</style>
