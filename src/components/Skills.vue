<template>
  <div id="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'>{{ index }}. {{ data.skill }}</li>
      </ul>

      <p v-if="skills.length >= 1">You have more than 1 skills</p>
      <p v-else>You have less than 1 skill</p>
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
        ]
      }
    } 
  }
</script>

<style scoped src="./Skills.css">
  
</style>
