<script>
  import faculties from '../../../data/main/faculties';
  import facultiesInfo from '../../../data/main/facultiesInfo';

  export default {
    name: 'Faculties',

    data(){
      return{
        faculties,
        facultiesInfo,
        title: "Faculties avaible at EduPrime",
        paragraph: "At single university with a load of courses, tailored to satisfy any student's needs",
        icon: 'fa-solid fa-sort-down',
        counter: 1
        }
      },

      methods:{
        change(i){
          this.counter = i;
        }
      }
  }
</script>

<template>
  <section class="faculties">
    <div class="text">
      <h2>{{ title }}</h2>

      <p>{{ paragraph }}</p>
    </div>

    <div class="row">
      <div
        class="col"
        :class="{'active' : index === counter}"
        v-for="(item, index) in faculties"
        :key="index"
        @click="change(index)">
        <img :src="item.imgSrc" :alt="item.text">

        <span>{{ item.text }}</span>

        <i :class="icon"></i>
      </div>
    </div>

    <div
      class="content"
      :class="{'visible' : index === counter - 1}"
      v-for="(illustration, index) in facultiesInfo"
      :key="index">
      <div class="container">
        <div class="image">
          <img :src="illustration.imgSrc" alt="Illustration">
        </div>

        <div class="low-faculty">
          <h3>{{ illustration.title }}</h3>

          <p>{{ illustration.paragraph }}</p>

          <button class="btn btn-red">{{ illustration.buttonText }}</button>
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
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: calc(100% / 7);
        height: 208px;
        border: 1px solid #eaeaea;
        padding: 30px 40px;
        cursor: pointer;
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

        &.active{
          color: $bg-white;
          background-color: $bg-red;

          i{
            display: block;
          }
        }

        i{
          display: none;
          position: absolute;
          bottom: -10px;
          left: 50%;
          transform: translate(-50%);
          font-size: 1.5rem;
        }
      }
    }

    .content{
      display: none;

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

      &.visible{
        display: block;
      }
    }
  }
</style>