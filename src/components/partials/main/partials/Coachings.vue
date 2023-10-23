<script>
  import coaching from '../../../../data/main/coaching';

  export default {
    name: 'Coachings',

    data(){
      return{
        coaching
      }
    }
  }
</script>

<template>
  <div class="col" v-for="(item, index) in coaching" :key="index">
    <div class="card">
      <h4>{{ item.title }}</h4>

      <span><i :class="item.icon"></i>{{ item.day }}</span>

      <p>{{ item.paragraph }}</p>

      <button class="btn btn-red"><i :class="item.buttonIcon"></i>{{ item.buttonText }}</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../../../../scss/variables.scss' as *;
  
  .col{
    padding: 20px;
    width: calc(100% / 3);

    .card{
      position: relative;
      border-radius: 10px;
      padding: 20px 40px;
      text-align: center;
      background-color: #fff;

      h4{
        margin-bottom: 15px;
      }

      span,
      p{
        color: #7f7f7f;
      }

      i{
        margin-right: 5px;
      }

      p{
        margin-top: 15px;
        margin-bottom: 30px;
        width: 100%;
      }

      .btn{
        position: absolute;
        bottom: -36px;
        left: 50%;
        padding: 20px 25px;
        transform: translate(-50%);
        box-shadow: 0px 0px 1px 0px #000;
      }
    }
  }
</style>