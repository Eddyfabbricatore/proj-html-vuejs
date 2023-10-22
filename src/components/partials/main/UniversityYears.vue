<script>
  export default {
    name: 'UniversityYears'
  }
</script>

<template>
  <div class="wave"></div>
  
  <section class="university-years">
    <div class="clock">
      <img src="../../../assets/img/Clock-and-Bell.png" alt="">
    </div>

    <div class="title">
      <h3>University Years</h3>
    </div>
  
    <div class="container">
      <div class="image">
        <img src="../../../assets/img/Timeline-Item.png" alt="">
      </div>

      <div class="demo-classes">
        <h5>Demo Classes</h5>

        <p>In the first week, students try to accommodate with the teaching style and choose their optional courses.</p>
      </div>

      <div class="graduation-day">
        <h5>Graduation Day</h5>

        <p>On the day of graduation, all students gather for the ceremony and then network and party among others.</p>
      </div>

      <div class="orientation">
        <h5>Orientation</h5>

        <p>First day of university year, all students gather fot the opening ceremony and then network with others.</p>
      </div>

      <div class="evaluation">
        <h5>Evaluation</h5>

        <p>At the end of a semester, students take a general evaluation test for every subject they're learning.</p>
      </div>
    </div>

    <div class="calendar">
      <img src="../../../assets/img/upcoming-events-calendar-icon.png" alt="">
    </div>
    
    <h3>Upcoming Events</h3>

    <div class="container">
      <div class="row">
        <div class="col">
          <div class="card">
            <h4>Coaching Sessions</h4>

            <span><i class="fa-regular fa-calendar-days"></i>20 May 21.30 PM</span>

            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>

            <button class="btn btn-red"><i class="fa-solid fa-plus"></i>Find More</button>
          </div>
        </div>

        <div class="col">
          <div class="card">
            <h4>Coaching Sessions</h4>

            <span><i class="fa-regular fa-calendar-days"></i>20 May 21.30 PM</span>

            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>

            <button class="btn btn-red"><i class="fa-solid fa-plus"></i>Find More</button>
          </div>
        </div>

        <div class="col">
          <div class="card">
            <h4>Coaching Sessions</h4>

            <span><i class="fa-regular fa-calendar-days"></i>20 May 21.30 PM</span>

            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>

            <button class="btn btn-red"><i class="fa-solid fa-plus"></i>Find More</button>
          </div>
        </div>
      </div>
    </div>

    <button class="btn btn-yellow">View All Events</button>
  </section>
  
  <div class="wave-last"></div>
</template>

<style lang="scss" scoped>
  @use '../../../scss/variables.scss' as *;

  .wave{
    height: 95px;
    background-image: url('../../assets/svg/svg-0.svg');
    background-size: cover;
  }

  .wave-last{
    height: 100px;
    background-image: url('../../assets/svg/svg-1.svg');
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