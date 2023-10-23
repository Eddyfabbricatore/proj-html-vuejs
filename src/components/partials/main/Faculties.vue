<script>
  import FacultyCard from './partials/FacultyCard.vue';
  import FacultyContent from './partials/FacultyContent.vue';

  export default {
    name: 'Faculties',

    components:{
      FacultyCard,
      FacultyContent
    },

    data(){
      return{
        title: "Faculties avaible at EduPrime",
        paragraph: "At single university with a load of courses, tailored to satisfy any student's needs",
        counter: 1
      }
    },

    methods:{
      change(i){
        this.counter = i;
      }
    }
  }
</script>

<template>
  <section class="faculties">
    <div class="text">
      <h2>{{ title }}</h2>

      <p>{{ paragraph }}</p>
    </div>

    <div class="row">
      <FacultyCard @changeFaculty="change" :counter="counter" />
    </div>

    <FacultyContent :counter="counter" />
  </section>
</template>

<style lang="scss" scoped>
  @use '../../../scss/variables.scss' as *;
  
  .faculties{
    margin-top: 180px;

    .text{
      display: flex;
      flex-direction: column;
      align-items: center;

      h2,
      p{
        margin-bottom: 40px; 
      }

      p{
        width: 350px;
        color: #454545;
      }
    }

    .row{
      display: flex;
      margin-bottom: 50px;
    }
  }
</style>