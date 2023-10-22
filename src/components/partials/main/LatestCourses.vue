<script>
  import courses from '../../../data/main/courses';
  import coursesMethod from '../../../data/main/coursesMethod';

  export default {
    name: 'LatestCourses',

    data(){
      return{
        courses,
        coursesMethod,
        title: 'Latest Courses',
      }
    }
  }
</script>

<template>
  <section class="latest-courses">
    <div class="container">
      <h2>{{ title }}</h2>

      <div class="row">
        <div class="col" v-for="(item, index) in courses" :key="index">
          <div class="card">
            <div class="image">
              <img :src="item.imgSrc" :alt="item.title">
            </div>

            <h5>{{ item.title }}</h5>

            <p><i :class="item.userIcon"></i>{{ item.role }}<span>{{ item.name }}</span></p>

            <p><i :class="item.moneyIcon"></i>{{ item.textPrice }}<span>{{ item.price }}</span></p>
          </div>
        </div>
      </div>

      <div class="content" v-for="(method, index) in coursesMethod" :key="index">
        <div class="text">
          <div class="image">
            <img :src="method.examImgSrc" alt="Exam">
          </div>

          <h2>{{ method.title }}</h2>

          <p>{{ method.paragraph }}</p>

          <button class="btn btn-red">{{ method.buttonText }}</button>
        </div>

        <div class="img">
          <img :src="method.imgSrc" alt="Illustration">
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  h2{
    margin-top: 50px;
  }

  .row{
    display: flex;
    margin-top: 50px;
    margin-bottom: 60px;
    width: 100%;

    .col{
      padding: 20px;
      width: calc(100% / 4);

      .card{
        display: flex;
        flex-direction: column;
        align-items: center;
        border-radius: 5px;
        padding: 20px;
        box-shadow: 1px 1px 5px 10px #f7f8fa;

        .image{
          margin-bottom: 20px;
          width: 50px;
          height: 50px;
        }

        h5,
        p{
          margin-bottom: 15px;
        }

        h5{
          font-size: 1.1rem;
          color: #223441
        }

        p{
          color: #8b8b8a;
        }

        i{
          margin-right: 5px;
        }

        span{
          color: #5c5e6c;
        }
      }
    }
  }

  .content{
    display: flex;
    width: 100%;

    .text,
    .img{
      width: 50%;
    }

    .text{
      .image{
        width: 70px;
        height: 70px;
      }

      h2,
      p{
        margin-bottom: 40px;
      }

      h2{
        margin-top: 20px;
      }

      p{
        font-size: 1.1rem;
        color: #434959;
      }
    }
    
    .img{
      padding: 50px;
    }

    &:last-of-type{
      flex-direction: row-reverse;
    }
  }
</style>