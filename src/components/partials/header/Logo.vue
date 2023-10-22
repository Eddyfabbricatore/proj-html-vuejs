<script>
  export default {
    name: 'Logo',

    props:{
      imgSrc: String
    }
  }
</script>

<template>
  <div class="logo">
    <img :src="imgSrc" alt="Logo EduPrime">
  </div>
</template>

<style lang="scss" scoped>
  .logo{
    width: 330px;
    height: 76px;
  }
</style>