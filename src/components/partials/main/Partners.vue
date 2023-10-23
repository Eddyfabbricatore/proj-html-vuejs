<script>
  import partners from '../../../data/main/partners';

  export default {
    name: 'Partners',

    data(){
      return{
        partners
      }
    }
  }
</script>

<template>
  <div class="partners">
    <div class="container">
      <h2>Partners</h2>

      <p>Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy.</p>

      <div class="row">
        <div class="col" v-for="(partner, index) in partners" :key="index">
          <img :src="partner.imgSrc" alt="Partners">
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
      color: #3d404f;
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
        
        img{
          opacity: .3;
          cursor: pointer;

          &:hover{
            opacity: 1;
          }
        }
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