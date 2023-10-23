<script>
  export default {
    name: 'Hero',

    data(){
      return{
        title: "Key to your success",
        paragraph: "EduPrime is the most versatile WorldPress theme for educational purposes, showcasing universities, curses, secondary scholls etc.",
        buttonYellowText: "Search Courses",
        buttonWhiteText: "Apply for university",
        search: "fa-solid fa-magnifying-glass",
        add: "fa-solid fa-user-plus",
        icons: ['fa-solid fa-cart-shopping', 'fa-solid fa-book-open', 'fa-solid fa-bullseye']
      }
    }
  }
</script>

<template>
  <div class="hero">
    <div class="menu">
      <i :class="icon" v-for="(icon, index) in icons" :key="index"></i>
    </div>

    <div class="content">
      <div class="text">
        <h1>{{ title }}</h1>

        <p>{{ paragraph }}</p>
      </div>

      <div class="btns">
        <div class="btn btn-yellow"><i :class="search"></i>{{ buttonYellowText }}</div>

        <div class="btn btn-white"><i :class="add"></i>{{ buttonWhiteText}}</div>
      </div>
    </div>

    <div class="wave">
      <div class="link">
        <span>Purchase EduPrime on Envato Market</span>
        
        <i class="fa-solid fa-sort-down"></i>
      </div>
    </div>
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
      position: absolute;
      left: 25px;
      top: 115px;
      transform: translate(-50%);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      border-top-right-radius: 5px;
      border-bottom-right-radius: 5px;
      padding: 15px 0;
      width: 50px;
      background-color: $bg-yellow;

      i{
        margin-bottom: 20px;
        cursor: pointer;
      }

      i:last-of-type{
        margin-bottom: 0;
      }
    }

    .content{
      width: 530px;

      .text{
        text-align: center;
  
        h1{
          margin-bottom: 30px;
        }

        p{
          margin-bottom: 40px;
          font-size: 1.1rem;
          color: #ffffffcc;
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

      .link{
        position: absolute;
        left: 50px;
        bottom: 0;
        border-radius: 5px;
        padding: 10px 20px;
        width: 300px;
        text-align: center;
        cursor: pointer;
        color: $bg-white;
        background-color: #151515;

        span{
          font-size: $p-size;
        }

        i{
          position: absolute;
          bottom: -5px;
          left: 50%;
          transform: translate(-50%);
          color: #151515;
        }
      }
    } 
  }
</style>