<script>
  import timeline from '../../../data/main/timeline';
  import Coachings from './partials/Coachings.vue';

  export default {
    name: 'UniversityYears',

    components:{
      Coachings
    },

    data(){
      return{
        timeline,
        clockImgSrc: "src/assets/img/Clock-and-Bell.png",
        title: "University Years",
        timelineImgSrc: "src/assets/img/Timeline-Item.png",
        calendarImgSrc: "/src/assets/img/upcoming-events-calendar-icon.png",
        secondTitle: "Upcoming Events",
        buttonText: "View All Events",
        }
    }
  }
</script>

<template>
  <div class="wave"></div>
  
  <section class="university-years">
    <div class="clock">
      <img :src="clockImgSrc" alt="Clock">
    </div>

    <div class="title">
      <h3>{{ title }}</h3>
    </div>
  
    <div class="container">
      <div class="image">
        <img :src="timelineImgSrc" alt="Timeline">
      </div>

      <div :class="item.class" v-for="(item, index) in timeline" :key="index">
        <h5>{{ item.title }}</h5>

        <p>{{ item.paragraph }}</p>
      </div>
    </div>

    <div class="calendar">
      <img :src="calendarImgSrc" alt="Calendar">
    </div>
    
    <h3>{{ secondTitle }}</h3>

    <div class="container">
      <div class="row">
        <Coachings />
      </div>
    </div>

    <div class="btns">
      <button class="btn btn-yellow">{{ buttonText }}</button>

      <button class="btn btn-red">{{ buttonText }}</button>
    </div>
  </section>
  
  <div class="wave-last"></div>
</template>

<style lang="scss" scoped>
  @use '../../../scss/variables.scss' as *;

  .wave{
    height: 95px;
    background-image: url('src/assets/svg/svg-0.svg');
    background-size: cover;
  }

  .wave-last{
    height: 100px;
    background-image: url('src/assets/svg/svg-1.svg');
    background-size: cover;
  }

  .university-years{
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: $bg-red;

    .clock,
    .calendar{
      width: 50px;
      height: 50px;
    }

    .clock{
      margin-top: 50px;
      margin-bottom: 15px;
    }

    .title{
      h3{
        margin-bottom: 140px;
        background-color: #db2a2c;
      }
    }

    .container{
      position: relative;

      p,
      h5{
        text-align: center;
      }

      h5{
        margin-bottom: 20px;
        color: #fff;
      }

      p{
        width: 360px;
        color: #ffffffcc;
      }

      .demo-classes{
        position: absolute;
        top: -115px;
        right: 535px;
      }

      .graduation-day{
        position: absolute;
        top: -115px;
        right: 50px;
      }

      .orientation{
        position: absolute;
        bottom: -115px;
        left: 50px;
      }

      .evaluation{
        position: absolute;
        bottom: -115px;
        left: 540px;
      }
    }

    .calendar{
      margin-top: 160px;
      margin-bottom: 20px;
    }

    h3{
      margin-bottom: 40px;
    }

    .row{
      display: flex;
      margin-bottom: 60px;
    }
   
    .btns{
      margin-bottom: 50px;

      .btn-red{
        display: none;
        background-color: $bg-red;
        box-shadow: 0px 0px 1px 0px #000;
      }

      &:hover{
        .btn-yellow{
          display: none;
        }

        .btn-red{
          display: block;
        }
      }
    }
  }
</style>