<script>
  import Logo from './partials/header/Logo.vue';
  import Menu from './partials/header/Menu.vue';
  import Hero from './partials/header/Hero.vue';

  export default {
    name: 'Header',

    components:{
      Logo,
      Menu,
      Hero
    }
  }
</script>

<template>
  <header id="top">
    <div class="top">
      <Logo imgSrc="/src/assets/img/theme_eduprime_logo.png" />

      <Menu buttonText="VIEW COURSES" />
    </div>

    <Hero
      title="Key to your success"
      paragraph="EduPrime is the most versatile WorldPress theme for educational purposes, showcasing universities, curses, secondary scholls etc."
      buttonYellowText="Search Courses"
      buttonWhiteText="Apply for university" />
  </header>
</template>

<style lang="scss" scoped>
  header{
    height: 530px;
    background-image: url('../assets/img/hero.png');
    background-size: cover;

    .top{
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 40px 0;
    }
  }
</style>