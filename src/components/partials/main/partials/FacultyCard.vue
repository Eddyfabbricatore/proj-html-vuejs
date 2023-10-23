<script>
  import faculties from '../../../../data/main/faculties';

  export default {
    name: 'FacultyCard',

    data(){
      return{
        faculties,
        icon: 'fa-solid fa-sort-down'
      }
    },

    props:{
      counter: Number
    }
  }
</script>

<template>
  <div
    class="col"
    :class="{'active' : index === counter}"
    v-for="(faculty, index) in faculties"
    :key="index"
    @click="$emit('changeFaculty', index)">
    <img :src="faculty.imgSrc" :alt="faculty.text">

    <span>{{ faculty.text }}</span>

    <i :class="icon"></i>
  </div>
</template>

<style lang="scss" scoped>
  @use '../../../../scss/variables.scss' as *;

  .col{
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border: 1px solid #eaeaea;
    padding: 30px 40px;
    width: calc(100% / 7);
    height: 208px;
    cursor: pointer;
    color: $bg-red;
    box-shadow: 0px 0px 10px 0px #eaeaea;

    img{
      margin-bottom: 10px
    }

    i{
      display: none;
      position: absolute;
      bottom: -8px;
      left: 50%;
      transform: translate(-50%);
      font-size: 1.5rem;
      color: $bg-red;
    }

    &.active{
      color: $bg-white;
      background-color: $bg-red;

      i{
        display: block;
      }
    }

    &:first-of-type,
    &:last-of-type{
      img,
      span,
      i{
        display: none;
      }
    }
  }
</style>