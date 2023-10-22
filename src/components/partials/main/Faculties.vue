<script>
  import faculties from '../../../data/main/faculties';

  export default {
    name: 'Faculties',

    data(){
      return{
        faculties
      }
    }
  }
</script>

<template>
  <section class="faculties">
    <div class="text">
      <h2>Faculties avaible at EduPrime</h2>

      <p>At single university with a load of courses, tailored to satisfy any student's needs</p>
    </div>

    <div class="row">
      <div class="col" v-for="(item, index) in faculties" :key="index">
        <img :src="item.imgSrc" :alt="item.text">

        <span>{{ item.text }}</span>
      </div>
    </div>

    <div class="content">
      <div class="container">
        <div class="image">
          <img src="../../../assets/img/Gavel-Illustration-e1556884768193.png" alt="">
        </div>

        <div class="low-faculty">
          <h3>Low Faculty</h3>

          <p>Learning from world-leading academics practitioners, you'll not only receive an outstanding grounding in the theory of low, but you will be able to undestand how those principles are applied in practice through a range of student-led activities and competitions.</p>

          <button class="btn btn-red">Read More</button>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  @use '../../../scss/variables.scss' as *;
  
  .faculties{
    margin-top: 180px;

    .text{
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;

      h2,
      p{
        margin-bottom: 40px; 
      }

      p{
        width: 350px;
        font-size: 1.1rem;
        color: #454545;
      }
    }

    .row{
      display: flex;
      margin-bottom: 50px;

      .col{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: calc(100% / 7);
        height: 208px;
        border: 1px solid #eaeaea;
        padding: 30px 40px;
        color: $bg-red;
        box-shadow: 0px 0px 10px 0px #eaeaea;

        img{
          margin-bottom: 10px;
        }

        &:first-of-type,
        &:last-of-type{
          img{
            display: none;
          }
        }
      }
    }

    .container{
      display: flex;
      justify-content: center;
      align-items: center;

      .image,
      .low-faculty{
        width: 50%;
      }

      .image{
        padding: 50px;
      }

      h3{
        margin-bottom: 30px;
        color: $h3-title;
      }

      p{
        margin-bottom: 50px;
        font-size: 1.1rem;
        color: #8b8b8a;
      }
    }
  }
</style>