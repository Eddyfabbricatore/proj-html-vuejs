<script>
  import timeline from '../../../data/main/timeline';
  import coaching from '../../../data/main/coaching';

  export default {
    name: 'UniversityYears',

    data(){
      return{
        timeline,
        coaching,
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
        <div class="col" v-for="(item, index) in coaching" :key="index">
          <div class="card">
            <h4>{{ item.title }}</h4>

            <span><i :class="item.icon"></i>{{ item.day }}</span>

            <p>{{ item.paragraph }}</p>

            <button class="btn btn-red"><i :class="item.buttonIcon"></i>{{ item.buttonText }}</button>
          </div>
        </div>
      </div>
    </div>

    <button class="btn btn-yellow">{{ buttonText }}</button>
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
        font-size: 1rem;
        color: #fff;
      }

      p{
        width: 360px;
        color: #fffffffc;
      }

      .demo-classes{
        position: absolute;
        top: -90px;
        right: 535px;
      }

      .graduation-day{
        position: absolute;
        top: -90px;
        right: 50px;
      }

      .orientation{
        position: absolute;
        bottom: -85px;
        left: 50px;
      }

      .evaluation{
        position: absolute;
        bottom: -85px;
        left: 540px;
      }
    }

    .calendar{
      margin-top: 140px;
      margin-bottom: 20px;
    }

    h3{
      margin-bottom: 40px;
    }

    .row{
      display: flex;
      margin-bottom: 60px;

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
            font-size: 1.2rem;
            color: #3d404f;
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
            box-shadow: 0px 1px 3px #000;
          }
        }
      }
    }

    .btn-yellow{
      margin-bottom: 50px;
    }
  }
</style>