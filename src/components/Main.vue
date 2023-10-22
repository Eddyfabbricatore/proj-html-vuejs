<script>
  import Courses from './partials/main/Courses.vue';
  import Faculties from './partials/main/Faculties.vue';
  import UniversityYears from './partials/main/UniversityYears.vue';
  import LatestCourses from './partials/main/LatestCourses.vue';
  import Subscribe from './partials/main/Subscribe.vue';
  import Partners from './partials/main/Partners.vue';

  export default {
    name: 'Main',

    components:{
      Courses,
      Faculties,
      UniversityYears,
      LatestCourses,
      Subscribe,
      Partners
    }
  }
</script>

<template>
  <main>
    <Courses />

    <Faculties />

    <UniversityYears />

    <LatestCourses />

    <Subscribe />

    <Partners />
  </main>
</template>

<style>
  main{
    margin-top: 10px;
  }
</style>