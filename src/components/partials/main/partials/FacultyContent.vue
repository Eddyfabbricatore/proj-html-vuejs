<script>
  import facultiesInfo from '../../../../data/main/facultiesInfo';

  export default {
    name: 'FacultyContent',

    data(){
      return{
        facultiesInfo
      }
    },

    props:{
      counter: Number
    }
  }
</script>

<template>
  <div
    class="content"
    :class="{'visible' : index === counter - 1}"
    v-for="(illustration, index) in facultiesInfo"
    :key="index">
    <div class="container">
      <div class="image">
        <img :src="illustration.imgSrc" :alt="illustration.title">
      </div>

      <div class="low-faculty">
        <h3>{{ illustration.title }}</h3>

        <p>{{ illustration.paragraph }}</p>

        <button class="btn btn-red">{{ illustration.buttonText }}</button>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../../../../scss/variables.scss' as *;

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
          color: #8b8b8a;
        }
      }

      &.visible{
        display: block;
      }
    }
</style>