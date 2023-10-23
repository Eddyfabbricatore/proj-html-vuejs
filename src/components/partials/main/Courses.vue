<script>
  export default {
    name: 'Courses',

    data(){
      return{
        bookImgSrc: "src/assets/img/Books-icon.png",
        title: "Thousands of courses for any type of student",
        paragraph: "At EduPrime, it doesn't matter what domain you wish to poursue a career in. Here you can find a course that satisfies your needs within a click away and applies for a course in a matter of minutes. EduPrime is ranked as the most versatile university in the world, thanks to the number of courses it provides.",
        buttonText: "Browse through courses",
        illustration: "src/assets/img/Graduation-Illustration.png"
      }
    }
  }
</script>

<template>
  <section class="courses">
    <div class="content">
      <div class="container">
        <div class="text">
          <div class="book">
            <img :src="bookImgSrc" alt="Book">
          </div>

          <h2>{{ title }}</h2>

          <p>{{ paragraph }}</p>

          <div class="btns">
            <button class="btn btn-yellow">{{ buttonText }}</button>

            <button class="btn btn-red">{{ buttonText }}</button>
          </div>
        </div>

        <div class="image">
          <img :src="illustration" alt="Illustration">
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .courses{
    height: 480px;

    .content{
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100%;
      background-image: url('../../../assets/img/home-background.png');
      background-size: cover;

      .container{
        display: flex;
        height: 100%;

        .text{
          margin-top: 50px;
          padding: 0 50px;
          width: 50%;

          .book{
            margin-bottom: 20px;
            width: 70px;
            height: 70px;
          }

          h2,
          p{
            margin-bottom: 30px;
          }

          .btn-red{
            display: none;
          }

          .btns:hover{
            .btn-yellow{
              display: none;
            }

            .btn-red{
              display: block;
            }
          }
        }

        .image{
          margin-top: 150px;
          margin-left: 30px;
          width: 480px;
          height: 330px;
        }
      }
    }
  }
</style>