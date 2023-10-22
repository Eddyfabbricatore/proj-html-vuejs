<script>
  export default {
    name: 'Partners'
  }
</script>

<template>
  <div class="partners">
    <div class="container">
      <h2>Partners</h2>

      <p>Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy.</p>

      <div class="row">
        <div class="col">
          <img src="../../../assets/img/partner-2.png" alt="">
        </div>

        <div class="col">
          <img src="../../../assets/img/partner-3.png" alt="">
        </div>

        <div class="col">
          <img src="../../../assets/img/partner-4.png" alt="">
        </div>

        <div class="col">
          <img src="../../../assets/img/partner-5.png" alt="">
        </div>

        <div class="col">
          <img src="../../../assets/img/partner-6.png" alt="">
        </div>

        <div class="col">
          <img src="../../../assets/img/partner-8.png" alt="">
        </div>

        <div class="col">
          <img src="../../../assets/img/partner-1.png" alt="">
        </div>

        <div class="col">
          <img src="../../../assets/img/partner-7.png" alt="">
        </div>
      </div>
    </div>
  </div>

  <div class="wave"></div>
</template>

<style lang="scss" scoped>
  @use '../../../scss/variables.scss' as *;
  
  .container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    h2{
      margin: 50px 0;
    }

    p{
      width: 450px;
      text-align: center;
      color: #434959;
    }

    .row{
      display: flex;
      justify-content: center;
      margin-top: 30px;
      margin-bottom: 100px;
      width: 100%;

      .col{
        padding: 10px;
        height: 70px;
      }
    }
  }

  .wave{
    height: 170px;
    background-image: url('../../../assets/img/background-wave3.png');
    background-size: cover;
    background-color: $last-wave;
  }
</style>