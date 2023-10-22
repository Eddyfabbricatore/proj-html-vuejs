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
    <Courses
      bookImgSrc="src/assets/img/Books-icon.png"
      title="Thousands of courses for any type of student"
      paragraph="At EduPrime, it doesn't matter what domain you wish to poursue a career in. Here you can find a course that satisfies your needs within a click away and applies for a course in a matter of minutes. EduPrime is ranked as the most versatile university in the world, thanks to the number of courses it provides."
      buttonText="Browse through courses"
      illustration="src/assets/img/Graduation-Illustration.png" />

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