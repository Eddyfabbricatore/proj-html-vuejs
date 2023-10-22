<script>
  export default {
    name: 'Courses',

    props:{
      bookImgSrc: String,
      title: String,
      paragraph: String,
      buttonText: String,
      illustration: String
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

          <button class="btn btn-yellow">{{ buttonText }}</button>
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