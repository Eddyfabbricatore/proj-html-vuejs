<script>
  import headerMenu from '../../../data/header/headerMenu';

  export default {
    name: 'Menu',

    data(){
      return{
        headerMenu
      }
    },

    props:{
      buttonText: String
    }
  }
</script>

<template>
  <div class="menu">
    <nav>
      <ul>
        <li v-for="(link, index) in headerMenu" :key="index">
          <a href="#">{{ link.text }} <i :class="link.icon"></i></a>
        </li>
      </ul>
    </nav>

    <div class="btns">
      <button class="btn btn-yellow">{{ buttonText }}</button>

      <button class="btn btn-white">{{ buttonText }}</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  @use '../../../scss/variables.scss' as *;

  .menu{
    display: flex;
    align-items: center;

    ul{
      display: flex;

      li{
        margin-right: 40px;

        a{
          display: flex;

          i{
            margin-left: 10px;
            font-size: .8rem;
          }

          &:hover{
            color: $bg-yellow;
          }
        }
      }
    }

    .btn-white{
      display: none;
    }

    .btns:hover{
      .btn-yellow{
        display: none;
      }

      .btn-white{
        display: block;
      }
    }
  }
</style>