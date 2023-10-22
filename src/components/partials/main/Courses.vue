<script>
  export default {
    name: 'Courses'
  }
</script>

<template>
  <section class="courses">
    <div class="content">
      <div class="container">
        <div class="text">
          <div class="book">
            <img src="../../../assets/img/Books-icon.png" alt="Book">
          </div>

          <h2>Thousands of courses for any type of student</h2>

          <p>At EduPrime, it doesn't matter what domain you wish to poursue a career in. Here you can find a course that satisfies your needs within a click away and applies for a course in a matter of minutes. EduPrime is ranked as the most versatile university in the world, thanks to the number of courses it provides.</p>

          <button class="btn btn-yellow">Browse through courses</button>
        </div>

        <div class="image">
          <img src="../../../assets/img/Graduation-Illustration.png" alt="">
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
          width: 50%;
        }

        .text{
          margin-top: 50px;
          padding: 0 50px;

          .book{
            width: 70px;
            height: 70px;
            margin-bottom: 20px;
          }

          h2,
          p{
            margin-bottom: 30px;
          }

          p{
            font-size: 1.1rem;
            color: #434959;
          }
        }

        .image{
          width: 480px;
          height: 330px;
          margin-top: 150px;
          margin-left: 30px;
        }
      }
    }
  }
</style>