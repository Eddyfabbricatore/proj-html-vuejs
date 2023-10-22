<script>
  export default {
    name: 'Hero',

    props:{
      title: String,
      paragraph: String,
      buttonYellowText: String,
      buttonWhiteText: String,
    }
  }
</script>

<template>
  <div class="hero">
    <div class="menu">
      <i class="fa-solid fa-cart-shopping"></i>

      <i class="fa-solid fa-book-open"></i>
    </div>

    <div class="content">
      <div class="text">
        <h1>{{ title }}</h1>

        <p>{{ paragraph }}</p>
      </div>

      <div class="btns">
        <div class="btn btn-yellow"><i class="fa-solid fa-magnifying-glass"></i>{{ buttonYellowText }}</div>

        <div class="btn btn-white"><i class="fa-solid fa-user-plus"></i>{{ buttonWhiteText}}</div>
      </div>
    </div>

    <div class="wave"></div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../../../scss/variables.scss' as *;
  
  .hero{
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 434px;
    color: #ffffffcc;

    .menu{
      display: flex;
      flex-direction: column;
      justify-content: center;
      text-align: center;
      position: absolute;
      left: 25px;
      top: 50%;
      transform: translate(-50%);
      border-top-right-radius: 5px;
      border-bottom-right-radius: 5px;
      width: 50px;
      background-color: #e9d758;

      i{
        margin-bottom: 20px;
      }
    }

    .content{
      width: 530px;

      .text{
        text-align: center;
  
        h1{
          margin-bottom: 30px;
          font-size: $h1-size;
        }

        p{
          margin-bottom: 40px;
          font-size: 1.1rem;
        }
      }

      .btns{
        display: flex;
        margin-bottom: 50px;

        .btn-yellow{
          margin-left: 75px;
          margin-right: 20px;
        }

        i{
          margin-right: 10px;
        }
      }
    }
    
    .wave{
      position: absolute;
      bottom: 0;
      width: 100%;
      height: 110px;
      background-image: url('../../../assets/img/Wave-1.png');
      background-size: cover;
    } 
  }
</style>