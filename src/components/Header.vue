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
  <header id="start">
    <div class="top">
      <Logo imgSrc="/src/assets/img/theme_eduprime_logo.png" />

      <Menu buttonText="VIEW COURSES" />
    </div>

    <Hero />
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